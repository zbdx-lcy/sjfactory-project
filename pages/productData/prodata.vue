<template>
	<view>
		<view class="bg">
			<view class="box">
				<view class="item" v-for="(item,index) in items" :key="index"> <!-- //最上面的不是空 -->
						<view class="text" v-if="ifshow(item)">
							<strong>产品数据{{index+1}}</strong>
							<br />
							<text>生产线：{{item.name}}\n沙棘果用量：{{item.scale}}\n沙棘汁瓶数：{{item.type}}\n沙棘果批次：{{item.dj}}\n工人工号：{{item.bzq}}\n生产日期：{{item.scrq}}</text>
						</view>
						<button type="primary" @click="clickbtn(index)">删除</button>
				</view>
			</view>
		</view>
		<uni-fab horizontal="right" vertical="bottom" @fabClick="fabClick"></uni-fab>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				items: [{}]
			};
		},
		onLoad() {
			uni.$on("PMinfo", (e) => {
				this.getText(e)
			})
		},
		mounted() {
			this.items = uni.getStorageSync("PROM");
			if (this.items[0] == null || this.items[0] == undefined) {
				this.items = [{
					name: "",
					scale: "",
					type: "",
					dj: "",
					bzq: "",
					scrq: ""
				}];
			}
		},
		methods: {
			ifshow(item) {
				if (item.name == '' && item.scale == '' && item.type == "" && item.dj == "" && item.bzq == "" && item
					.scrq == "") {
					return false;
				} else {
					return true;
				}
			},
			getText(e) {
				this.items.push(e);
				uni.setStorageSync("PROM", this.items);
			},
			clickbtn(index) {
				uni.showModal({
					title: "操作提示",
					content: "确定要删除此条数据吗？",
					cancelColor: "#007aff",
					success: (e) => {
						if (e.confirm) {
							this.items.splice(index, 1);
							uni.setStorageSync("PROM", this.items);
						}
					}
				})
			},
			fabClick() {
				uni.navigateTo({
					url: "/pages/productData/addproData"
				})
			}
		}
	}
</script>

<style lang="scss">
	.bg {
		border-top: #cccccc 1rpx solid;
		background-color: #F1F1F1;
		width: 750rpx;
		height: 100vh;
		overflow: auto;

		.box {
			display: flex;
			justify-content: space-around;
			flex-wrap: wrap;
			align-items: flex-start;
		}

		.item {
			margin-top: 15rpx;
			margin-bottom: 15rpx;
			width: 90%;
			height: 410rpx;
			background-color: #fff;
			display: flex;
			border-radius: 25rpx;

			.text {
				font-size: 42rpx;
				padding: 25rpx;

				text {
					font-size: 32rpx;
				}
			}

			button {
				margin-top: 150rpx;
				margin-right: 30rpx;
				width: 125rpx;
				height: 75rpx;
				font-size: 30rpx;
				background-color: #fb9f28;
			}
		}
	}
</style>
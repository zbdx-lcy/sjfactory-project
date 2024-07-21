<template>
	<view>
		<!-- 沙棘数据 -->
		<view class="text">
			<view class="item">
				<text>产线序号</text>
				<input type="number" @input="get1" />
			</view>
			<view class="item">
				<text>沙棘果批次</text>
				<input type="text" @input="get2" />
			</view>
			<view class="item">
				<text>总数量</text>
				<input type="number" @input="get3" />
			</view>
			<view class="item">
				<text>破损数量</text>
				<input type="number" @input="get4" />
			</view>
			<button type="primary" @click="confirm">确认</button>
		</view>

	</view>
</template>

<script>
	export default {
		data() {
			return {
				name: "",
				time: "",
				posi: "",
				type: "",
			}
		},
		methods: {
			get1(e) {
				this.name = e.detail.value;
			},
			get2(e) {
				this.time = e.detail.value;
			},
			get3(e) {
				this.posi = e.detail.value;
			},
			get4(e) {
				this.type = e.detail.value;
			},
			confirm() {
				uni.$emit("SJinfo", {
					name: this.name,
					time: this.time,
					sum: this.posi,
					deadnum: this.type
				});
				uni.navigateBack({
					delta: 1
				});
			}
		}
	}
</script>

<style lang="scss">
	.text {
		margin-top: 120rpx;
		margin-left: 40rpx;
		margin-right: 40rpx;

		.item {
			margin-top: 80rpx;

			input {
				margin-top: 10rpx;
				margin-bottom: 10rpx;
				border-bottom: gray solid 2rpx;
				padding-bottom: 1rpx;
				font-size: 35rpx;
			}

			text {
				font-size: 37rpx;
			}
		}

		button {
			margin-top: 70rpx;
			background-color: #fb9f28;
		}
	}
</style>
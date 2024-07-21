<template>
	<view>
		<view class="bg">
			<view class="box">
				<view class="item" v-for="(item,index) in items" :key="index">
				<view class="text" v-if="ifshow(item)">
					<strong>{{item.name}}</strong>
					<br />
					<text>姓名：{{item.id}}\n异常行为次数：{{item.scale}}\n应发工资：{{item.pos}}\n实发工资：{{item.type}}\n扣款额：{{calculateSalary(item)}}</text>
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
				items:[{}]
			};
		},
		onLoad() {
			uni.$on("FACinfo",(e)=>{
				this.getText(e);
			})
		},
		mounted() {
			this.items=uni.getStorageSync("FACM");
			 if (this.items[0] == null || this.items[0] == undefined) {
			     this.items=[{id:"",name:"",scale:"",pos:"",type:""}];
			 }	
		},
		methods:{
			calculateSalary(item) {
			    if (isNaN(item.pos) || isNaN(item.type) || item.pos === 0) {
			        return 0;
			    } else {
			        return item.pos - item.type;
			    }
			},
			ifshow(item) {
				if (item.name == '' && item.scale == '' && item.pos == "" && item.id == "" && item.type == "") {
					return false;
				} else {
					return true;
				}
			},
			getText(e){
				this.items.push(e);
				uni.setStorageSync("FACM",this.items);
			},
			clickbtn(index){
				uni.showModal({
					title:"操作提示",
					content:"确定要删除此条数据吗？",
					cancelColor:"#007aff",
					success: (e) => {
						if(e.confirm){
							this.items.splice(index, 1);
							uni.setStorageSync("FACM",this.items);
						}
					}
				})
			},
			fabClick(){
				uni.navigateTo({
					url:"/pages/factorymanage/addfactory"
				})
			}
		}
	}
</script>

<style lang="scss">
.bg{
	border-top: #cccccc 1rpx solid;
	background-color: #F1F1F1;
	width: 750rpx;
	height:100vh;
	overflow: auto;
	.box{
		margin-top: 20rpx;
		display: flex;
		justify-content: space-around;
		flex-wrap: wrap;
		align-items: flex-start;
	}	
	.item{
		margin-top: 15rpx;
		margin-bottom: 15rpx;
		width: 90%;
		height: 340rpx;
		background-color: #fff;
		display: flex;
		border-radius: 25rpx;
		.text{
			font-size: 42rpx;
			padding: 25rpx;
			text{
				font-size: 32rpx;
			}
		}
		button{
			margin-top: 120rpx;
			margin-right:  30rpx ;
			width: 125rpx;
			height: 75rpx;
			font-size: 30rpx;
			background-color: #fb9f28;
		}
	}
}
</style>

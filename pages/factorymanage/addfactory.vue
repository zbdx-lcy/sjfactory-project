<template>
	<view>
		<!-- 没实现传参 -->
		<view class="text" >
			<view class="item">
				<text>工号</text>
				<input type="number" @input="get1"/>
			</view>
			<view class="item">
				<text>姓名</text>
				<input type="text" @input="get5"/>
			</view>
			<view class="item">
				<text>异常行为次数</text>
				<input type="number" @input="get2"/>
			</view>
			<view class="item">
				<text>应发工资</text>
				<input type="number" @input="get3"/>
			</view>
			<view class="item">
				<text>实发工资</text>
				<input type="number" @input="get4"/>
			</view>
			<button type="primary" @click="confirm">确认</button>
		</view>
		
	</view>
</template>

<script>
	export default {
		data() {
			return {
				name:"",
				scale:"",
				posi:"",
				type:"",
				id:""
			}
		},
		methods: {
			get1(e){
				this.name=e.detail.value;
			},
			get2(e){
				this.scale=e.detail.value;
			},
			get3(e){
				this.posi=e.detail.value;
			},
			get4(e){
				this.type=e.detail.value;
			},
			get5(e){
				this.id=e.detail.value;
			},
			confirm(){
				uni.$emit("FACinfo",{name:this.name,scale:this.scale,pos:this.posi,type:this.type,id:this.id});
				uni.navigateBack({delta:1});
			}
		}
	}
</script>

<style lang="scss">
.text{
	margin-top: 120rpx;
	margin-left: 40rpx;
	margin-right: 40rpx;
	.item{
		margin-top: 80rpx;
		input{
			margin-top: 10rpx;
			margin-bottom: 10rpx;
			border-bottom: gray solid 2rpx;
			padding-bottom: 1rpx;
			font-size: 35rpx;
		}
		text{
			font-size: 37rpx;
		}
	}
	button{
		background-color: #fb9f28;
		margin-top: 70rpx;
	}
}

</style>

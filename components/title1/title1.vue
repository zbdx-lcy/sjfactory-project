<template>
	<view class="title">
		{{title}}
	</view>
</template>

<script>
	export default {
		name:"title1",
		props:{
			title:{
				type:String,
				default:"默认标题"
			},
		},
		data() {
			return {
				
			};
		}
	}
</script>

<style lang="scss">
.title {
		color: #000000;
		font-weight: bold;
		font-size: 50rpx;
		display: flex;
		justify-content: space-around;
		box-sizing: border-box;
		margin-top: 80rpx;
		margin-bottom: 100rpx;
	}
</style>
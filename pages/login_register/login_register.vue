<template>
	<view>
		<h1 class="title1"> 高效管理&nbsp;一点就好</h1>
		<h5 class="subtitle">你好,欢迎使用智慧沙棘</h5>
		<view class="zm">
			<view class="z">
				<image src="/static/zh.png" mode="aspectFit"></image>
				<input type="digit" @input="setid" placeholder="请输入您的账号" />
			</view>
			<br />
			<view class="m">
				<image src="../../static/mm.png" mode="aspectFit"></image>
				<input type="safe-password" password="text" @input="setpw" placeholder="请输入您的密码" />
			</view>

		</view>

		<view class="btn">
			<button style="color: white; background-color: #1AAD19; width: 310rpx; line-height:70rpx;"
				@click="doLogin"><text style="font-size: 36rpx;">登录</text></button>
		</view>

		<view class="xia">
			<view class="forget">
				忘记密码
			</view>
			<view class="regis" @click="doRegist">
				注册
			</view>
		</view>


	</view>
</template>

<script>
	export default {
		data() {
			return {
				iid: "",
				ipassword: "",
				id: "",
				password: "",
				ui: "", //用户序号
				unum: 2, //注册++
				check: false
			};
		},
		methods: {
			doLogin() {
				this.unum = uni.getStorageSync("unum");
				for (var i = 0; i <= this.unum; i++) {
					this.ui = "u" + i;
					let a = uni.getStorageSync(this.ui);
					this.id = a.id;
					this.password = a.password;
					if (this.id == this.iid && this.password == this.ipassword) {
						this.check = true;
						uni.switchTab({
							url: "/pages/mainpage/mainpage"
						});
						break;
					}
				}
				if (this.check == false) {
					uni.showModal({
						title: "登录失败",
						content: "用户名或密码错误，请重试！",
						showCancel: false
					})
				}
			},
			doRegist() {
				uni.navigateTo({
					url: "/pages/login_register/register"
				})
			},
			setid(e) {
				this.iid = e.detail.value;
			},
			setpw(e) {
				this.ipassword = e.detail.value;
			}
		},
		mounted() {
			uni.setStorageSync("u0", {
				id: "2213041523",
				password: "123456"
			})
			uni.setStorageSync("u1", {
				id: "2113043126",
				password: "123456"
			})
			//uni.setStorageSync("u2",{id:"2113043126",password:"123456"})	
		}
	}
</script>

<style lang="scss">
	.subtitle {
		text-align: center;
		margin-bottom: 100rpx;
		font-weight: normal;
		font-size: 30rpx;
	}
	.title1 {
		font-family: "STXingkai" "华文隶书";
		color: #000000;
		//font-weight: bold;
		font-size: 58rpx;
		display: flex;
		justify-content: space-around;
		box-sizing: border-box;
		margin-top: 240rpx;
		margin-bottom: 30rpx;
	}

	.zm {
		display: flex;
		flex-direction: column;
		//align-items: flex-end;
		margin-left: 60rpx;
		margin-right: 60rpx;
		height: 300rpx;

		input {
			height: 100rpx;
			font-size: 36rpx;
			padding-left: 30rpx;
			line-height: 80rpx;
		}
		.z {
			display: flex;
			image {
				width: 70rpx;
				height: 70rpx;
				padding-top: 15rpx;
			}
			border-bottom: #1AAD19 solid 1rpx;
		}

		.m {
			display: flex;
			image {
				width: 60rpx;
				height: 60rpx;
				padding-top: 17rpx;
			}

			;
			border-bottom: #1AAD19 solid 1rpx;
		}
	}

	.btn {
		margin: 280rpx 40rpx 20rpx 40rpx;
	}
.xia {
	display: flex;
	flex-direction: row;
	justify-content: center;
	font-size: 27rpx;
	.forget {
		color: #0556d7;
		font-size: 30rpx;
	}
	.regis {
		padding-left: 30rpx;	
		color: #0556d7;
		font-size: 30rpx;
	}
}
	
</style>
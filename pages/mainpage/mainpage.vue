<template>
	<view class="bg">
		<view class="topchart">
			<image src="../../static/chart2.png" style="width: 94%;" mode="aspectFit"></image>
		</view>

		<!-- 新闻 -->
		<view class="news">
			<swiper class="swip" :vertical="true" :autoplay="true" :circular="true" :interval="2000"
				display-multiple-items="1" style="background-color: #FFFFFF; border-radius: 10rpx;">
				<swiper-item class="item">
					<view class="item-content">
						<image src="../../static/news.png" style="height: 60rpx;width: 60rpx;" mode="aspectFit"></image>
						<text class="item-text"
							style="white-space: nowrap; overflow: hidden !important; text-overflow: ellipsis !important;">
							山西浑源：小沙棘变身“致富果”
						</text>
					</view>
					<view class="separator">></view>
				</swiper-item>

				<swiper-item class="item">
					<view class="item-content">
						<image src="../../static/news.png" style="height: 60rpx;width: 60rpx;" mode="aspectFit"></image>
						<text class="item-text"
							style="white-space: nowrap; overflow: hidden !important; text-overflow: ellipsis !important;">
							山西交城：沙棘产业拓宽群众致富路
						</text>
					</view>
					<view class="separator">></view>
				</swiper-item>
				<swiper-item class="item">
					<view class="item-content">
						<image src="../../static/news.png" style="height: 60rpx;width: 60rpx;" mode="aspectFit"></image>
						<text class="item-text"
							style="white-space: nowrap; overflow: hidden !important; text-overflow: ellipsis !important;">
							浮山县：沙棘饮品出深山 电商直播来添翼
						</text>

					</view>
					<view class="separator">></view>
				</swiper-item>
				<swiper-item class="item">
					<view class="item-content">
						<image src="../../static/news.png" style="height: 60rpx;width: 60rpx;" mode="aspectFit"></image>
						<text class="item-text"
							style="white-space: nowrap; overflow: hidden !important; text-overflow: ellipsis !important;">
							小众沙棘果 “破圈”销全国
						</text>

					</view>
					<view class="separator">></view>
				</swiper-item>
				<swiper-item class="item">
					<view class="item-content">
						<image src="../../static/news.png" style="height: 60rpx;width: 60rpx;" mode="aspectFit"></image>
						<text class="item-text"
							style="white-space: nowrap; overflow: hidden !important; text-overflow: ellipsis !important;">
							新疆沙棘产业缘何迎来“艳阳天”
						</text>

					</view>
					<view class="separator">></view>
				</swiper-item>
				<swiper-item class="item">
					<view class="item-content">
						<image src="../../static/news.png" style="height: 60rpx;width: 60rpx;" mode="aspectFit"></image>
						<text class="item-text"
							style="white-space: nowrap; overflow: hidden !important; text-overflow: ellipsis !important;">
							沙棘变“新宠” 成就兵地产业“传奇”
						</text>

					</view>
					<view class="separator">></view>
				</swiper-item>
				<swiper-item class="item">
					<view class="item-content">
						<image src="../../static/news.png" style="height: 60rpx;width: 60rpx;" mode="aspectFit"></image>
						<text class="item-text"
							style="white-space: nowrap; overflow: hidden !important; text-overflow: ellipsis !important;">
							沙棘——中国最不矫情的水果
						</text>

					</view>
					<view class="separator">></view>
				</swiper-item>
				<swiper-item class="item">
					<view class="item-content">
						<image src="../../static/news.png" style="height: 60rpx;width: 60rpx;" mode="aspectFit"></image>
						<text class="item-text"
							style="white-space: nowrap; overflow: hidden !important; text-overflow: ellipsis !important;">
							沙棘产业前景广阔 仍需技术创新
						</text>

					</view>
					<view class="separator">></view>
				</swiper-item>
				<swiper-item class="item">
					<view class="item-content">
						<image src="../../static/news.png" style="height: 60rpx;width: 60rpx;" mode="aspectFit"></image>
						<text class="item-text"
							style="white-space: nowrap; overflow: hidden !important; text-overflow: ellipsis !important;">
							发展沙棘产业——生态果变成黄金果
						</text>

					</view>
					<view class="separator">></view>
				</swiper-item>
				<swiper-item class="item">
					<view class="item-content">
						<image src="../../static/news.png" style="height: 60rpx;width: 60rpx;" mode="aspectFit"></image>
						<text class="item-text"
							style="white-space: nowrap; overflow: hidden !important; text-overflow: ellipsis !important;">
							沙棘林里种“幸福”
						</text>

					</view>
					<view class="separator">></view>
				</swiper-item>
				<swiper-item class="item">
					<view class="item-content">
						<image class="item-image" src="../../static/news.png" mode="aspectFit"></image>
						<text class="item-text"
							style="white-space: nowrap; overflow: hidden !important; text-overflow: ellipsis !important;">
							“酸果果”变身“金豆豆”，小沙棘做出大文章
						</text>

					</view>
					<view class="separator">></view>
				</swiper-item>
			</swiper>
		</view>

		<view class="duoyuan">
			<view class="multiyuan">
				<view class="jiacu">多元数据</view>
				<view class="row">
					<view class="item" @click="video">
						<image src="/static/Jvideo.png" style="height: 80rpx;" mode=""></image>
						<text>实时视频</text>
					</view>
					<view class="item" @click="livePigMage">
						<image src="/static/shaij.png" mode=""></image>
						<text>沙棘数据</text>
					</view>
					<view class="item" @click="moneyMage">
						<image src="/static/moneydata.png" mode=""></image>
						<text>财务数据</text>
					</view>
					<view class="item" @click="materialMage">
						<image src="/static/productData.png" style="width: 80rpx; height: 75rpx;" mode=""></image>
						<text style="padding-top: 15rpx;">产品数据</text>
					</view>
				</view>
			</view>
		</view>

		<view class="ribao">
			<view class="rbgy">
				<view class="jiacu">日报概要</view>
				<view class="row">
					<view class="item" @click="video">
						<text style="font-size: 40rpx;">2845</text>
						<text style="color: #888888;">产出总数</text>
					</view>
					<view class="item" @click="livePigMage">
						<text style="font-size: 40rpx;">123</text>
						<text style="color: #888888;">原料破损</text>
					</view>
					<view class="item" @click="moneyMage">
						<text style="font-size: 40rpx;">94%</text>
						<text style="color: #888888;">工人专注</text>
					</view>
					<view class="item" @click="materialMage">
						<text style="font-size: 40rpx;">47</text>
						<text style="color: #888888;">出勤人数</text>
					</view>
				</view>
			</view>
		</view>

		<view class="hangqing">
			<view class="jrhq">
				<view class="hqtop">
					<view class="jiacu">今日行情</view>
					<view class="posi">
						<picker mode="selector" :range="array" :value="index" @change="bindPickerChange">
							<view>{{array[index]}}</view>
						</picker>
						<image class="arrow-icon" src="/static/arrow-down.png"></image>
					</view>
				</view>

				<view class="row">
					<view class="item" @click="video">
						<text style="font-size: 35rpx; color: #fb9f28;">13.4元</text>
						<text style="color: #4D4D4D;">沙棘果(斤)</text>
					</view>
					<view class="item" @click="livePigMage">
						<text style="font-size: 35rpx; color: #fb9f28;">17元</text>
						<text style="color: #4D4D4D;">沙棘原浆(斤)</text>
					</view>
					<view class="item" @click="moneyMage">
						<text style="font-size: 35rpx; color: #fb9f28;">4.5元</text>
						<text style="color: #4D4D4D;">沙棘汁(瓶)</text>
					</view>
				</view>
				<view class="btmchart">
					<image src="../../static/chart.png" mode=""></image>
				</view>
			</view>
			
		</view>


	</view>
</template>

<script>
	import chart1 from "../../components/chart/chart1.vue" // 假设组件路径为 components/Chart1.vue
	export default {
		components: {
			chart1
		},
		data() {
			return {
				title: 'picker',
				array: ['太原市', '大同市', '阳泉市', '长治市', '晋城市', '朔州市', '晋中市', '运城市', '忻州市', '临汾市', '吕梁市'],
				index: 0,
				pieData: [{
						name: '沙棘果总数',
						value: 100
					},
					{
						name: '完好数',
						value: 70
					},
					{
						name: '破损数',
						value: 30
					}
				],
				canvasStyle: {
					width: '300rpx',
					height: '300rpx'
				},
				colors: ['#FFC107', '#4CAF50', '#F44336']
			}
		},
		methods: {
			livePigMage() {
				uni.navigateTo({
					url: "/pages/shajiData/sjData"
				})
			},
			video() {
				uni.navigateTo({
					url: "/pages/video/video"
				})
			},
			moneyMage() {
				uni.navigateTo({
					url: "/pages/moneyMage/moneyMage"
				})
			},
			materialMage() {
				uni.navigateTo({
					url: "/pages/productData/prodata"
				})
			}
		}
	}
</script>

<style lang="scss">
	.btmchart {
		padding-top: 0px;
		margin-top: 0px;
		display: flex;
		justify-content: center;
		height: 240px;
	}
	.topchart {
		padding-top: 10px;
		margin-top: 0px;
		display: flex;
		justify-content: center;
		height: 230px;
	}
	.container {
		display: flex;
		justify-content: center;
		align-items: center;
		height: 100vh;
	}

	.pie-chart {
		width: 300px;
		height: 300px;
	}

	.legend {
		margin-left: 20px;
	}

	.legend-item {
		display: flex;
		align-items: center;
		margin-bottom: 5px;
	}

	.legend-color {
		width: 10px;
		height: 10px;
		margin-right: 5px;
	}

	.legend-text {
		font-size: 12px;
	}

	.news {
		display: flex;
		justify-content: center;
		.swip {
			height: 120rpx;
			width: 94%;

			.item {
				display: flex;
				padding-left: 20rpx;
				align-items: center;
				height: 30rpx;

				.item-content {
					.item-image {
						height: 51rpx;
						width: 51rpx;
					}

					.item-text {
						padding-left: 20rpx;
						padding-top: 10rpx;
						font-size: 32rpx;
						color: #505050;
						width: 560rpx;
					}
					display: flex;
				}
				.separator {
					margin-right: 10px;
					font-size: 38rpx;
					/* 根据需要调整大小 */
					line-height: 30rpx;
					/* 竖直方向居中 */
					color: #505050 !important;
				}
			}
		}
	}

	.duoyuan {
		display: flex;
		justify-content: center;
		align-items: center;
		margin-top: 20rpx;

		.multiyuan {
			.row {
				margin-top: 25rpx;
				display: flex;
				justify-content: space-around;

				.item {
					display: flex;
					flex-direction: column;

					text {
						padding-top: 10rpx;
						font-size: 30rpx;
					}
				}

				image {
					padding-left: 20rpx;
					height: 80rpx;
					width: 80rpx;
				}
			}

			background-color: #fff;
			border-radius: 10rpx;
			width: 94%;
			margin-bottom: 30rpx;
			padding-bottom: 20rpx;

			.jiacu {
				font-weight: bold;
				font-size: 36rpx;
				border-bottom: #cacaca 1rpx solid;
				padding: 20rpx 0 23rpx 20rpx;
			}
		}
	}

	.ribao {
		display: flex;
		justify-content: center;
		align-items: center;
		//margin-top: 20rpx;

		.rbgy {
			.row {
				margin-top: 30rpx;
				display: flex;
				justify-content: space-around;

				.item {
					display: flex;
					flex-direction: column;

					text {
						text-align: center;
						padding-top: 10rpx;
						font-size: 30rpx;
					}
				}

				image {
					padding-left: 20rpx;
					height: 80rpx;
					width: 80rpx;
				}
			}

			background-color: #fff;
			border-radius: 10rpx;
			width: 94%;
			margin-bottom: 30rpx;
			padding-bottom: 20rpx;

			.jiacu {
				font-weight: bold;
				font-size: 36rpx;
				border-bottom: #cacaca 1rpx solid;
				padding: 20rpx 0 23rpx 20rpx;
			}
		}
	}

	.hangqing {
		display: flex;
		justify-content: center;
		align-items: center;

		.jrhq {
			.hqtop {
				display: flex;
				justify-content: space-between;

				.picker-wrapper {
					display: flex;
					align-items: center;
				}

				.posi {
					display: flex;
					padding: 20rpx 20rpx 0rpx 20rpx;

					picker {
						padding-right: 10rpx;
					}
				}

				.picker-text {
					flex: 1;
					font-size: 32rpx;
					color: #000000;
				}

				.arrow-icon {
					padding-top: 5rpx;
					width: 30rpx;
					height: 30rpx;
				}

			}

			.row {
				margin-top: 10rpx;
				display: flex;
				justify-content: space-around;
				margin-bottom: 20rpx;
				padding-bottom: 15rpx;
				border-bottom: #cacaca 1rpx solid;
				
				.item {
					display: flex;
					flex-direction: column;
					background-color: #eeeeee;
					padding: 18rpx;
					border-radius: 20rpx;
					text {
						text-align: center;
						padding-top: 10rpx;
						font-size: 30rpx;
					}
				}

				image {
					padding-left: 20rpx;
					height: 80rpx;
					width: 80rpx;
				}
			}

			background-color: #fff;
			border-radius: 10rpx;
			width: 94%;
			margin-bottom: 50rpx;
			padding-bottom: 20rpx;

			.jiacu {
				font-weight: bold;
				font-size: 36rpx;
				padding: 20rpx 0 0rpx 20rpx;

			}
		}
	}

	.bg {
		border-top: #cccccc 1rpx solid;
		background-color: #F1F1F1;
	}

	.swiper {
		width: 100%;
		height: 510rpx;

		.item {
			box-sizing: border-box;
		}

		image {
			width: 100%;
			height: 510rpx;
		}
	}



	.recom {
		margin-top: 30rpx;
		box-sizing: border-box;
		padding: 15rpx 20rpx 10rpx 20rpx;
		width: 100%;
		height: 750rpx;
		background-color: #F1F1F1;
		border: black;

		.title {
			display: flex;
			justify-content: space-between;
			margin-top: 20rpx;

			.bold {
				font-weight: bold;
				font-size: 35rpx;
			}
		}

		.pic {
			display: flex;
			flex-wrap: wrap;

			.item {
				width: 280rpx;
				height: 150rpx;
				display: flex;
				background-color: #fff;
				padding: 30rpx;
				margin-top: 60rpx;
				margin-left: 15rpx;

				.text {
					font-size: 30rpx;
					margin-right: 30rpx;
					margin-top: 13rpx;
				}

				image {

					width: 100rpx;
					height: 100rpx;
				}
			}
		}

	}
</style>
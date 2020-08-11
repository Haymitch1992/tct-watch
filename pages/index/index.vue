<template>
	<view class="content">
		<view class="uni-margin-wrap">
			<swiper class="swiper" :disable-programmatic-animation="false" circular :indicator-dots="indicatorDots"  :interval="interval" :duration="duration" @change="longshock">
				<swiper-item>
					<!-- 到站信息 -->
					<view class="swiper-item uni-bg-a" style="font-size: 12px;">
						<view class="current-time">17:20</view>
						<view class="current-station">
							<text class="tip">本站</text>
							<text>白石桥南</text>
						</view>
						<view class="station-flex-box">
							<view class="station-info">
								<view class="top">开往方向</view>
								<view class="bottom">国家图书馆</view>	
							</view>
							<view class="station-info">
								<view class="top">到站剩余</view>
								<view class="bottom">3分钟</view>	
							</view>
						</view>
						<view>
							<text class="car-status car-status-start car-status-1">1</text>
							<text class="car-status car-status-2">2</text>
							<text class="car-status car-status-3">3</text>
							<text class="car-status car-status-4">4</text>
							<text class="car-status car-status-3">5</text>
							<text class="car-status car-status-3">6</text>
							<text class="car-status car-status-1">7</text>
							<text class="car-status car-status-end car-status-2">8</text>
						</view>
					</view>
				</swiper-item>
				<swiper-item>
					<!-- 行程进程 -->
					<view class="swiper-item uni-bg-b" style="font-size: 14px;">
						<view class="swiper-item uni-bg-a" style="font-size: 12px;">
							<view class="current-time">17:20</view>
							<view class="next-station-info">
								<text>距</text>
								<text class="strong">丰台科技园站</text>
								<text>还剩</text>
								<text class="strong">3</text>
								<text>站</text>
							</view>
							<view class="next-station-time">
								<text>剩余</text>
								<text class="strong">12</text>
								<text>分钟</text>
							</view>
							<view class="car-title">车厢拥挤程度</view>
							<view>
								<text class="car-status car-status-start car-status-1">1</text>
								<text class="car-status car-status-2">2</text>
								<text class="car-status car-status-3">3</text>
								<text class="car-status car-status-4">4</text>
								<text class="car-status car-status-3">5</text>
								<text class="car-status car-status-3">6</text>
								<text class="car-status car-status-1">7</text>
								<text class="car-status car-status-end car-status-2">8</text>
							</view>
						</view>
					</view>
				</swiper-item>
				<swiper-item>
					<!-- 下车提醒 -->
					<view class="swiper-item uni-bg-c" style="font-size: 20px;">
						<view class="swiper-item uni-bg-a" style="font-size: 12px;">
						<view class="current-time">17:20</view>
						<view class="current-station">
							<text class="tip">本站</text>
							<text>白石桥南</text>
						</view>
						<view class="station-flex-box">
							<view class="station-info">
								<view class="top">开往方向</view>
								<view class="bottom">国家图书馆</view>	
							</view>
							<view class="station-info">
								<view class="top">到站剩余</view>
								<view class="bottom">3分钟</view>	
							</view>
						</view>
						<view>
							<text class="car-status car-status-start car-status-1">1</text>
							<text class="car-status car-status-2">2</text>
							<text class="car-status car-status-3">3</text>
							<text class="car-status car-status-4">4</text>
							<text class="car-status car-status-3">5</text>
							<text class="car-status car-status-3">6</text>
							<text class="car-status car-status-1">7</text>
							<text class="car-status car-status-end car-status-2">8</text>
						</view>
					</view>
					</view>
				</swiper-item>
				<swiper-item>
					<!-- 招援求助 -->
					<view class="swiper-item uni-bg-c" style="font-size: 20px;">
						<switch checked />
					</view>
				</swiper-item>
				<swiper-item>
					<!-- 求助成功 -->
					<view class="swiper-item uni-bg-e" style="font-size: 28px;">28px</view>
				</swiper-item>
			</swiper>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				title: 'Hello',
				background: ['color1', 'color2', 'color3','color1', 'color2',],
				indicatorDots: true,
				autoplay: true,
				interval: 1000,
				duration: 400
			}
		},
		onLoad() {

		},
		methods: {
			longshock() {
				// uni.vibrateLong({
				// 	success: function() {
				// 		console.log('success');
				// 	}
				// });
			},
			changeIndicatorDots(e) {
				this.indicatorDots = !this.indicatorDots
			},
			changeAutoplay(e) {
				this.autoplay = !this.autoplay
			},
			intervalChange(e) {
				this.interval = e.detail.value
			},
			durationChange(e) {
				this.duration = e.detail.value
			}
		}
	}
</script>

<style>
	uni-swiper .uni-swiper-wrapper{
	}
	.uni-margin-wrap {
		width:100%;
	}
	.swiper {
		height: 750rpx;
	}
	.swiper-item {
		display: block;
		height: 750rpx;
		text-align: center;
	}

	.swiper-list {
		margin-top: 40rpx;
		margin-bottom: 0;
	}

	.uni-common-mt{
		margin-top:60rpx;
		position:relative;
	}
	
	.uni-bg-a{
		background-color: #000000;
		color: #FFFFFF;
	}
	.uni-bg-b{
		background-color: #000000;
	}
	.uni-bg-c{
		background-color: #000000;
	}
	.uni-bg-d{
		background-color: #4CD964;
	}
	.uni-bg-e{
		background-color: #F0AD4E;
	}
	.current-time{
		padding-top: 20rpx;
		font-size: 40rpx;
	}
	.current-station{
		background-color: #FADB34;
		color: #000000;
		box-shadow: inset 7px 7px 16px #d7bc2d, 
		            inset -7px -7px 16px #fffa3b;
		display: inline-block;
		margin: 0 auto;
		border-radius: 100px;
		font-size: 50rpx;
		margin-top: 60rpx;
		padding: 20rpx 50rpx;
	}
	.current-station .tip{
		font-size: 30rpx;
		vertical-align: super;
		margin-right: 10px;
	}
	.car-status{
		width: 60rpx;
		height: 60rpx;
		background-color: #007AFF;
		margin-right: 4px;
		display: inline-block;
		line-height: 60rpx;
		border-radius: 4px;
	}
	.car-status-start{
		border-top-left-radius: 10px;
		width: 80rpx;
	}
	.car-status-end{
		border-top-right-radius: 10px;
		width: 80rpx;
	}
	.station-info{
		color: #ffdd6a;
		font-size: 50rpx;
		width: 50%;
		flex: 1;
	}
	.station-info .bottom{
		color: #FFFFFF;
		padding: 10px 0;
		font-size: 46rpx;
	}
	.station-flex-box{
		display: flex;
		padding: 30px 0;
	}
	.car-status-1{
		/* 拥挤程度低 */
		background-color: #4dd39a;
	}
	.car-status-2{
		/* 拥挤程度中 */
		background-color: #fadc3a;
	}
	.car-status-3{
		/* 拥挤程度高 */
		background-color: #fea12f;
	}
	.car-status-4{
		/* 拥挤程度极高 */
		background-color: #fd6f62;
	}
	uni-swiper .uni-swiper-dot{
		background-color: #ccc;
	}
	uni-swiper .uni-swiper-dot-active{
		background-color: #FFFFFF;
	}
	.next-station-info{
		font-size: 50rpx;
		margin-top: 174rpx;
		color: #ffdd6a;
	}
	.next-station-time{
		font-size: 50rpx;
		margin-top: 30rpx;
		margin-bottom: 50rpx;
		color: #ffdd6a;
	}
	.next-station-info .strong{
		margin: 0 4px;
		color: #FFFFFF;
	}
	.next-station-time .strong{
		margin: 0 4px;
		color: #FFFFFF;
	}
	.car-title{
		font-size: 32rpx;
		text-align: left;
		padding-left: 80rpx;
		padding-bottom: 14rpx;
	}
</style>

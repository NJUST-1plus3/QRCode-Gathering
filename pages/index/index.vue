<template>
	<view class="content">
		<!-- 消息通知栏 -->
		<van-notice-bar 
			left-icon="volume-o" 
			scrollable
			class="notice-bar"
			:text="text"/>
		<!-- 使用介绍 -->
		<view class="details">
			<image src="../../static/images/index.jpg"></image>
		</view>
		<view class="row1">
			<view class="row1_1">
				<image src="../../static/images/wx-pay1.jpg" mode="widthFix" @click="showQRCode(1)"/>
			</view>
			<view class="row1_2">
				<view class="row1_2_item" >
					<image src="../../static/images/ali-pay1.jpg" @click="showQRCode(2)">
				</view>
				<view class="row1_2_item" >
					<image src="../../static/images/id-code1.jpg" @click="showQRCode(3)"/>
				</view>	
			</view>
		</view>
		<van-divider/>
		<view class="row2">
			<view class="row2-item">
				<image src="../../static/img/wx-health1.jpg" @click="showQRCode(4)"/>
			</view>
			<view class="row2-item">
				<image src="../../static/img/ali-health1.jpg" @click="showQRCode(5)"/>
			</view>
		</view>
		<van-dialog
		  use-slot
		  title="收款码"
		  :show="show"
		  @close="onClose"
		>
		  <image :src="showImg" />
		</van-dialog>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				text: '小程序 （汇码）QRCodeGathering 1.0v 正式上线啦 ！',
				show: false,
				showImg: ''
			}
		},
		onLoad() {

		},
		methods: {
			showQRCode(e) {
				console.log("show qrcode~~~~");
				this.show = !this.show;
				console.log(e);
				switch(e) {
					case 1:
						this.showImg = "../../static/images/wx-pay2.jpg";
						console.log("~~~~~~~~~~~~~~~~");
						break;
					case 2:
						this.showImg = "../../static/images/ali-pay2.jpg";
						console.log(this.showImg);
						break;
					case 3:
						this.showImg = "../../static/images/id-code2.jpg";
						break;
					case 4:
						this.showImg = "../../static/images/wx-health2.jpg";
						break;
					case 5:
						this.showImg = "";
						break;
				}
			},
			onClose() {
				this.show = !this.show;
			}
		}
	}
</script>

<style lang="scss">
	.content {
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
		background-color: $uni-bg-color;
	}
	.notice-bar {
		width: 100%;
	}
	.details image {
		width: 750rpx;
		height: 400rpx;
		border-radius: 30rpx;
		margin-top: 5rpx;
	}
	.row1 {
		width: 730rpx;
		height: 400rpx;
		display: flex;
		flex-direction: row;
		justify-content: space-around;
		.row1_1 {
			margin-top: 5rpx;
			width: 350rpx;
			height: 400rpx;
			image {
				width: 350rpx;
				height: 350rpx;
				border-radius: 20rpx;
			}
		}
		.row1_2 {
			width: 350rpx;
			height: 475rpx;
			display: flex;
			flex-direction: column;
			justify-content: space-between;
			.row1_2_item {
				margin-top: 5rpx;
				height: 200rpx;
				image {
					width: 350rpx;
					height: 225rpx;
					border-radius: 20rpx;
				}
			}
		}
	}
	.row2 {
		margin-top: 40rpx;
		width: 750rpx;
		height: 250rpx;
		display: flex;
		flex-direction: row;
		justify-content: space-around;
		.row2-item {
			width: 350rpx;
			image {
				width: 350rpx;
				height: 250rpx;
				border-radius: 20rpx;
			}
		}
	}	
</style>

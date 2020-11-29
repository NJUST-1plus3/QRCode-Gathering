<template>
	<view class="content">
		<view class="user-info">
			<view class="user-detail" @click="toUserDetails">
				<view class="user-icon">
					<image :src="userInfo.imgSrc"></image>
				</view>
				<view class="user-name">
					{{userInfo.name}}
				</view>
			</view>
		</view>
		<view class="user-other">
			<view class="other-item">
				<view class="other-item-info">
					<van-icon name="service-o" size="40rpx" color="#f57018"/>
					<text>联系客服</text>
					<view class="arrow"><van-icon name="arrow"/></view>
				</view>
			</view>
			<view class="divLine"></view>
			<view class="other-item">
				<view class="other-item-info">
					<van-icon name="exchange" size="40rpx" color="#f57018"/>
					<text>意见反馈</text>
					<view class="arrow"><van-icon name="arrow" /></view>
				</view>
			</view>
			<view class="divLine"></view>
			<view class="other-item">
				<view class="other-item-info">
					<van-icon name="friends-o" size="40rpx" color="#f57018"/>
					<text>关于我们</text>
					<view class="arrow"><van-icon name="arrow" /></view>
				</view>
			</view>
			<view class="divLine"></view>
			<view class="other-item">
				<view class="other-item-info">
					<van-icon name="share-o" size="40rpx" color="#f57018"/>
					<text @click="onClick">分享给朋友</text>
					<van-share-sheet
					  :show="showShare"
					  title="立即分享给好友"
					  :options="options"
						@select="onSelect"
						@close="onClose"
					/>
					<view class="arrow"><van-icon name="arrow" /></view>
				</view>
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				showShare: false,
				userInfo: {
					name: "汇码",
					imgSrc: "../../static/logo.png"
				},
				options: [
					[
						{ name: '微信', icon: 'wechat' },
						{ name: '微博', icon: 'weibo' },
						{ name: 'QQ', icon: 'qq' },
					],
					[
						{ name: '复制链接', icon: 'link' },
						{ name: '分享海报', icon: 'poster' },
						{ name: '二维码', icon: 'qrcode' },
					],
				],
			}
		},
		onLoad() {

		},
		methods: {
			onClick () {
				this.showShare = true
			},
			onClose () {
				this.showShare = false
			},
			onSelect (event) {
				Toast(event.detail.name);
				this.onClose();
			},
			toUserDetails() {
				uni.navigateTo({
					url: "../user_details/user_details",
					success: (res) => {
						console.log(res);
					}
				})
			}
		}
	}
</script>

<style lang="scss">
	page{
		background-color: $uni-bg-color;
	}
	.content {
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
	}
	.user-info {
		width: 750rpx;
		height: 400rpx;
		background-color: $uni-theme-color;
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
	}
	.user-detail {
		height: 200rpx;
		.user-icon image{
			width: 140rpx;
			height: 140rpx;
		}
		.user-name {
			height: 60rpx;
			font-size: large;
			color: white;
			text-align: center;
			margin-top: 20rpx;
		}
	}
	.user-other {
		width: 730rpx;
		height: 400rpx;
		margin: 10rpx 10rpx 0rpx 10rpx;
		border-radius: 20rpx;
		display: flex;
		flex-direction: column;
		background-color: #FFFFFF;
		.other-item {
			margin-top: 1rpx;
			height: 80rpx;
			padding: 10rpx;
			text {
				margin-left: 10rpx;
			}
			.arrow {
				float: right;
			}
		}
	}
	.divLine{
	 background: #E0E3DA;
	 width: 100%;
	 height: 5rpx;
	}
	
</style>

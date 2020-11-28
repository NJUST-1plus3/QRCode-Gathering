<template>
	<view class="content">
		<view class="card">
			<view class="title">登记注册</view>
			<view class="contact">
				<input placeholder="请输入您的昵称" />
			</view>
			 <view class="contact">
				<input placeholder="输入您的邮箱地址" /></br>
			</view>
			<view class="uploader">
				请上传您的微信付款码： 
				<van-uploader></van-uploader> </br>
				请上传您的支付宝付款码：
				<van-uploader></van-uploader> </br>
			</view>		
		</view>
		<!--底部确认-->
		<button class="confirm">注册并登录</button>
		<view class="shen_title">
			<image class="about" src="../../static/icon/about.png" />使用申明
		</view>
		<view class="des">1. 请确保手机号和邮箱百分百有效，之后将用于发送实时订单通知。</view>
		<view class="des">2. 在未经您同意及确认之前，本程序不会将您的注册信息用于任何其它商业目的。</view>
		<view class="des">3. 本程序将对您所提供的资料进行严格的管理及保护，本程序将使用相应的技术，防止您的个人资料丢失、被盗用或遭篡改。</view>
		<view class="des">4. 请您放心使用！</view>
	</view>
</template>

<script>
</script>

<style>
	.top-bg {
		position: absolute;
		top: 0rpx;
		left: 0rpx;
		width: 100%;
		height: 460rpx;
		background-repeat: no-repeat;
		background-size: 100%;
	}
	
	.contain {
		position: absolute;
		top: 176rpx;
		left: 0rpx;
		width: 100%;
		padding: 0rpx 40rpx 0rpx 40rpx;
		box-sizing: border-box;
	}
	
	.card {
		border-radius: 32rpx;
		width: 100%;
		background: #fff;
		padding: 50rpx 60rpx;
		box-sizing: border-box;
		box-shadow: 0 0 20rpx #eee;
	}
	
	.title {
		width: 100%;
		text-align: center;
		font-size: 40rpx;
		font-weight: 600;
		letter-spacing: 6rpx;
	}
	
	.phone {
		justify-content: space-between;
		margin-top: 45rpx;
		width: 100%;
		height: 92rpx;
		background: #f1f3f8;
		border-radius: 10rpx;
		text-align: left;
		padding: 0 20rpx 0 36rpx;
		box-sizing: border-box;
		font-size: 32rpx;
		display: flex;
		align-items: center;
		color: #8c9aa8;
		border: none;
	}
	
	.phone::after {
		border: none;
	}
	
	.campus {
		margin-top: 24rpx;
		width: 100%;
		height: 92rpx;
		background: #f1f3f8;
		border-radius: 10rpx;
		text-align: left;
		padding: 0 20rpx 0 36rpx;
		box-sizing: border-box;
		font-size: 32rpx;
		display: flex;
		align-items: center;
		justify-content: space-between;
		color: #8c9aa8;
	}
	
	.right {
		width: 30rpx;
		height: 30rpx;
	}
	
	.contact {
		margin-top: 24rpx;
		width: 100%;
		height: 92rpx;
		background: #f1f3f8;
		border-radius: 10rpx;
		text-align: left;
		padding: 0 36rpx;
		box-sizing: border-box;
		font-size: 32rpx;
		display: flex;
		align-items: center;
		justify-content: space-between;
		color: #8c9aa8;
	}
	
	.contact input {
		width: 100%;
		height: 100%;
	}
	
	.uploader {
		margin-top: 10rpx;
	}
	
	.pache {
		font-size: 32rpx;
		color: #8c9aa8;
	}
	
	.confirm {
		margin-top: 50rpx;
		width: 100%;
		height: 100rpx;
		display: flex;
		justify-content: center;
		align-items: center;
		background: linear-gradient(#00aa00, #19CAAD);
		border-radius: 60rpx;
		color: #fff;
		font-size: 40rpx;
		letter-spacing: 4rpx;
		box-shadow: 0 0 20rpx #eee;
		border: none;
	}
	.confirm::after {
		border: none;
	}
	.shen_title{
		margin-top: 40rpx;
		font-size: 32rpx;
		letter-spacing: 2rpx;
		display: flex;
		justify-content: flex-start;
		align-items: center;
	}
	.about{
		width: 32rpx;
		height: 32rpx;
		padding-right: 10rpx;
	}
	.des{
		padding-left: 30rpx;
		padding-top: 20rpx;
		font-size: 26rpx;
		color: #acacac;
		letter-spacing: 2rpx;
		line-height: 42rpx;
	}
</style>

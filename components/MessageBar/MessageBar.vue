<template>
	<view id="MessagebarPage">
		<view class="left">
			<span class="uesrImage">
				<img src="@/static/image/touxiang.jpg" alt="" />
				<view class="dot">11</view>
			</span>
		</view>
		<view class="right">
			<view class="">
				<span class="userName">爱吃草莓</span>
				<span class="userTime">晚上8:17</span>
			</view>
			<view class="userMessage">你好</view>
		</view>
	</view>
</template>

<script>
export default {
	name: 'MessageBar',
	data() {
		return {};
	}
};
</script>

<style lang="scss">
.flexBeCenter {
	display: flex;
	justify-content: space-between;
	align-items: center;
}
#MessagebarPage {
	display: flex;
	// @extend .flexBeCenter;
	height: 7.535421vh;
	// line-height: 7.26vh;
	padding: 0 0.9719222vh;
	margin-bottom: 10px;
	& > .left {
		display: flex;
		align-items: center;
		margin-right: 2.803738vw;
		& > .uesrImage {
			position: relative;
			display: inline-block;
			height: 12.882242vw;
			width: 12.882242vw;
			& > img {
				border-radius: 10px;
			}
			& > .dot {
				font-size: 10px;
				color: #fff;
				text-align: center;
				position: absolute;
				top: 0;
				right: 0;
				width: 4.572897vw;
				height: 4.572897vw;
				line-height: 4.572897vw;
				background-color: red;
				border-radius: 50%;
				transform: translate(50%, -50%);
			}
		}
	}
	& > .right {
		display: flex;
		flex-direction: column;
		flex: 1;
		justify-content: space-between;
		padding-bottom: 2vw;
		border-bottom: 1px solid #c0c0c0;
		& > view:nth-child(1) {
			width: 100%;
			flex: 1;
			@extend .flexBeCenter;
			& > span:nth-child(1) {
				font-size: 19px;
			}
			& > span:nth-child(2) {
				font-size: 14px;
				color: #a8a8a8;
				margin-right: 6.074766vw;
			}
		}
		& > view:nth-child(2) {
			font-size: 15px;
			color: #a8a8a8;
		}
	}
}
</style>

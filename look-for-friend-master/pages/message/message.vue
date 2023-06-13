<template>
	<view id="messagePage">
		<view class="header">
			<view class="content">
				<view class="left">
					<span @click="tabChange(0)" :class="{ changeFontSize: topTabIndex == 0 }">
						<span>
							好友
							<view class="dot" v-show="topTabIndex !== 0"></view>
						</span>
						{{ topTabIndex == 0 ? '（' + topTabIndex + '）' : '' }}
					</span>
					<span @click="tabChange(1)" :class="{ changeFontSize: topTabIndex == 1 }">
						<span>
							群聊
							<view class="dot" v-show="topTabIndex !== 1"></view>
						</span>
						{{ topTabIndex == 1 ? '（' + topTabIndex + '）' : '' }}
					</span>
				</view>
				<view class="right">
					<img src="@/static/image/notice.png" alt="">
				</view>
			</view>
		</view>
		<view class="content">
			<MessageBar></MessageBar>
			<MessageBar></MessageBar>
			<MessageBar></MessageBar>
			<MessageBar></MessageBar>
		</view>
		<view class="footer">
			<Tabbar :tabIndex="tabIndex"></Tabbar>
		</view>
	</view>
</template>

<script>
export default {
	data() {
		return {
			tabIndex: 0,
			topTabIndex: 0
		};
	},
	methods: {
		tabChange(e) {
			// console.log(e);
			this.topTabIndex = e;
		}
	},
	onLoad() {}
};
</script>

<style lang="scss">
.flexBeCenter {
 display: flex;
 justify-content: space-between;
 align-items: center;
}	
#messagePage {
	// position: relative;
	height: 100vh;
	background: url('@/static/image/bg_one.png') 100% 100% no-repeat;

	& > .header {
		width: 100%;
		height: 7.06vh;

		display: flex;
		align-items: center;
		justify-content: center;
		background-color: transparent;
		& > .content {
			width: 87.61vw;
			height: 3.24vh;
			line-height: 3.24vh;
			font-size: 17px;
			@extend .flexBeCenter;
			
			& > .left {
				display: inline-block;
			}
			& > .right {
				width: 5.84vw;
				height: 5.84vw;
				display: inline-block;
			}
			& > .left > .changeFontSize {
				font-size: 20px;
				font-weight: 600;
			}
			& > .left > span > span {
				position: relative;
			}
			& > .left > span > span .dot {
				position: absolute;
				top: 0;
				right: -0.5vw;
				width: 2.34vw;
				height: 2.34vw;
				border-radius: 50%;
				background-color: #e8585a;
			}
			& > .left > span:nth-child(1) {
				margin-right: 2.804vw;
			}
		}
	}
	& > .content {
		height: 93vh;
		padding-top:1.159827vh;;
	}

	& > .footer {
		width: 100%;
		height: auto;
		position: fixed;
		bottom: 0;
	}
}
</style>

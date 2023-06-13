<template>
	<view id="personPage">
		<view class="uesrInfoBox">
			<view class="setting">
				<img src="@/static/image/setting.png" alt="" />
			</view>
			<view class="userInfo">
				<view class="userImgAndBaseInfo">
					<img src="@/static/image/touxiang.jpg" alt="二维码" />
					<view class="baseInfo">
						<view class="userAliasName">院子爱吃草莓</view>
						<view class="userName">
							<span>姓名：阿萨德</span>
							<span>
								<img src="@/static/image/address.png" alt="二维码" />
							</span>
						</view>
						<view class="userID">寻觅号：396475</view>
					</view>
				</view>
				<view class="userAddressAndIntroduce">
					<view class="address">
						<span class="imgIcon">
							<img src="@/static/image/address.png" alt="位置" />
						</span>
						干嘛
					</view>
					<view class="introduce">
						<span class="imgIcon">
							<img src="@/static/image/love.png" alt="个人介绍" />
						</span>
						在哪
					</view>
				</view>
			</view>
		</view>

		<view class="function">
			<view class="fucntion--main">
				<ul>
					<li>
						<view class="">
							<img src="@/static/image/CircleFriends.png" alt="" />
						</view>
						<view class="">朋友圈</view>
					</li>
					<li>
						<view class="">
							<img src="@/static/image/notice.png" alt="" />
						</view>
						<view class="">好友列表</view>
					</li>
					<li>
						<view class="">
							<img src="@/static/image/circle.png" alt="" />
						</view>
						<view class="">圈子</view>
					</li>
				</ul>
			</view>
			<view class="function--sub">
				<view class="fucntionName">娱乐中心</view>
				<view class="item-row">
					<ul>
						<li>
							<view class="">
								<img src="@/static/image/karaoke.png" alt="" />
							</view>
							<view class="">KTV</view>
						</li>
						<li>
							<view class="">
								<img src="@/static/image/ScriptKill.png" alt="" />
							</view>
							<view class="">剧本杀</view>
						</li>
						<li>
							<view class="">
								<img src="@/static/image/InternetBars.png" alt="" />
							</view>
							<view class="">玩吧</view>
						</li>
					</ul>
				</view>
				<view class="item-row">
					<ul>
						<li>
							<view class="">
								<img src="@/static/image/karaoke.png" alt="" />
							</view>
							<view class="">KTV</view>
						</li>
						<li>
							<view class="">
								<img src="@/static/image/ScriptKill.png" alt="" />
							</view>
							<view class="">剧本杀</view>
						</li>
						<li>
							<view class="">
								<img src="@/static/image/InternetBars.png" alt="" />
							</view>
							<view class="">玩吧</view>
						</li>
					</ul>
				</view>
				<view class="item-row">
					<ul>
						<li>
							<view class="">
								<img src="@/static/image/karaoke.png" alt="" />
							</view>
							<view class="">KTV</view>
						</li>
						<li>
							<view class="">
								<img src="@/static/image/ScriptKill.png" alt="" />
							</view>
							<view class="">剧本杀</view>
						</li>
						<li>
							<view class="">
								<img src="@/static/image/InternetBars.png" alt="" />
							</view>
							<view class="">玩吧</view>
						</li>
					</ul>
				</view>
				
			</view>
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
			tabIndex: 2
		};
	},
	onLoad() {},
	methods: {}
};
</script>

<style lang="scss">
.flexBeCenter {
	display: flex;
	justify-content: space-between;
	align-items: center;
}
#personPage {
	height: 100vh;
	background: url('@/static/image/bg_two.png') 100% 100% no-repeat;
	background-size: cover;
	& > .uesrInfoBox {
		width: 100vw;
		height: 35.097192vh;
		color: rgb(104, 104, 104);
		background:url("@/static/image/bg_three.png") 100% 100% no-repeat ;
		& > .setting {
			height: 6.587473vh;
			

			display: flex;
			align-items: center;
			justify-content: right;

			padding-right: 9.813084vw;
			
			background-color: #d6cdcf;;
			& > img {
				height: 6.542056vw;
				width: 6.542056vw;
			}
		}
		& > .userInfo {
			padding-left: 4.672897vw;
			padding-top: 1.187904vh;
			& > .userImgAndBaseInfo {
				display: flex;
				align-items: center;
				& > img {
					width: 26.869158vw;
					height: 26.869158vw;
					border-radius: 50%;
				}
				& > .baseInfo {
					padding-left: 2.336448vw;
					display: inline-block;
					& > view {
						margin-bottom: 0.61111vh;
					}
					& > .userAliasName {
						height: fit-content;
						color: black;
						font-size: 28px;
						font-weight: 400;
					}
					& > .userName {
						display: flex;

						& > span:nth-child(2) {
							display: inline-block;
							width: 4.672897vw;
							height: 4.672897vw;
							margin-left: 10.514018vw;
						}
					}
					& > .userID {
					}
				}
			}
			& > .userAddressAndIntroduce {
				margin-top: 2.375809vh;
				& > view {
					display: flex;
					align-items: center;
					margin-bottom: 1.61987vh;
				}
				& > view > span {
					display: inline-block;
					height: 6.542056vw;
					width: 6.542056vw;
					margin-right: 1vw;
				}
			}
		}
	}

	& > .function {
		width: 100vw;
		height: 45.032397vh;
		& > .fucntion--main {
			padding: 0 8.17757vw;
			height: 9.935205vh;
			background-color: #fff;
			border-top-left-radius: 3vw;
			border-top-right-radius: 3vw;
			display: flex;
			align-items: center;
			justify-content: center;
			
			opacity: 0.95;
			& > ul {
				width: 100vw;
				@extend .flexBeCenter;
				& > li {
					// text-align: center;
					display: flex;
					flex-direction: column;
					align-items: center;
					& > view:nth-child(1) {
						width: 7.042253vw;
						height: 7.042253vw;
						margin-bottom: 0.9vw;
					}
				}
			}
		}

		& > .function--sub {
			width: inherit;
			height: 35.097192vh;
			padding: 5.939524vh 0;
			background-color: #fff;
			position: relative;

			border-top: 1px solid rgba(223, 223, 223, 0.8);
			display: flex;
			justify-content:space-between;
			flex-direction: column;
			
			border-bottom-left-radius: 6vw;
			border-bottom-right-radius: 6vw;
			
			opacity: 0.9;
			& > .fucntionName {
				position: absolute;
				top: 1.295896vh;
				left: 4.672897vw;
				font-size: 17px;
				color: #ababab;
			}

			& >.item-row {
				width: 100vw;
				height: 6.57149vh;
				padding: 0 8.644859vw;
				& > ul {
					width: 100%;
					@extend .flexBeCenter;
					& > li {
						// text-align: center;
						display: flex;
						flex-direction: column;
						align-items: center;
						& > view:nth-child(1) {
							width: 7.042253vw;
							height: 7.042253vw;
							margin-bottom: 0.9vw;
						}
					}
				}

			}
		}
	}

	& > .footer {
		width: 100%;
		height: auto;
		position: fixed;
		bottom: 0;
	}
}
</style>

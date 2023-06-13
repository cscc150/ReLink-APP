<template>
	<view id="outer">
		<ul>
			<li @click="tabChange(0)">
				<span>
					<img src="@/static/image/tabber/message_avtive.png" alt="消息">
				</span>
				<span :style="tabColorChoosed == 0 ? 'color:#FA541C' : 'color:black'">消息</span>
			</li>
			<li @click="tabChange(1)">
				<span>
					<img src="@/static/image/tabber/message_avtive.png" alt="MAP">
				</span>
				<span :style="tabColorChoosed == 1 ? 'color:#FA541C' : 'color:black'">MAP</span>
			</li>
			<li @click="tabChange(2)">
				<span>
					<img src="@/static/image/tabber/person_center.png" alt="我的">
				</span>
				<span :style="tabColorChoosed == 2 ? 'color:#FA541C' : 'color:black'">我的</span>
			</li>
		</ul>
	</view>
</template>

<script>
export default {
	name: 'Tabbar',
	data() {
		return {
			tabColorChoosed: 0,
		};
	},
	props:{
		tabIndex:{
			type: Number,
			required: true,
		}
	},
	methods: {
		tabChange(index) {
			// this.tabColorChoosed=index
			// console.log(index);
			switch(index){
				case 0:
				uni.navigateTo({
					url:'/pages/message/message?index=0'
				})
				break;
				case 1:
				uni.navigateTo({
					url:'/pages/MAP/MAP?index=1'
				})
				break;
				case 2:
				uni.navigateTo({
					url:'/pages/index/index?index=2'
				})
				break;
			}
		},
	},
	onLoad:function(){
		
	},
	beforeMount() {
		this.tabColorChoosed=this.tabIndex
	}
};
</script>

<style lang="scss">
#outer {
	width: 100%;
	height: 5.94vh;
	background-color: #ffffff; 

	& > ul {
		display: inline-block;
		width: inherit;
		height: inherit;
		padding: 0 2.99vh;
		display: flex;
		justify-content: space-between;
		align-items: center;
		& > li {
			font-size: 15px;
			height: inherit;
			display: flex;
			flex-direction: column;
			justify-content: space-around;
			align-items: center;
			&>span:nth-child(1){
				width: 2.36vh;
				min-width: 24px;
				height: 2.36vh;
				min-height: 24px;
			}
		}
	}
}
</style>

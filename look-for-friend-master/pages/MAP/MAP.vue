<template>
	<view id="mapPage">
		MAP
		<!-- <u-button type="primary" text="确定"></u-button> -->
		<!-- <u-action-sheet></u-action-sheet> -->
		<view class="footer">
			<Tabbar :tabIndex="tabIndex"></Tabbar>
		</view>
	</view>
</template>

<script>
export default {
	data() {
		return {
			tabIndex: 1
		};
	},
	onLoad: function () {}
};
</script>

<style lang="scss">
#mapPage {
	& > .footer {
		width: 100%;
		height: auto;
		position: fixed;
		bottom: 0;
	}
}
</style>

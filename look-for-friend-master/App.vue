<script>
export default {
	onLaunch: function () {
		console.log('App Launch');
	},
	onShow: function () {
		console.log('App Show')

	},
	onHide: function () {
		console.log('App Hide');
	}
};
</script>

<style lang="scss">
/*每个页面公共css */
/* uni.scss */
* {
	padding: 0;
	margin: 0;
	box-sizing: border-box;
}
li {
	list-style-type: none;
}
img {
	width: 100%;
	height: 100%;
}
</style>

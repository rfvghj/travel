<template>
<div class="header">
	城市选择
	<router-link to="/">
		<div class="iconfont header-back">&#xe624;</div>
</router-link>
</div>
</template>

<script>
export default {
  name: 'CityHeader'
}
</script>

<style lang="stylus" scoped>
@import '~styles/varibles.styl'
	.header
		position:relative
		overflow:hidden
		height:$headerHeight
		line-height:$headerHeight
		text-align:center
		background-color:$bgColor
		color:#fff
		font-size:.32rem
		.header-back
			position:absolute
			width:.64rem
			top:0
			left:0
			color:#fff
			font-size:.4rem
			
			
</style>

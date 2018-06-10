<template>
	<div>
		<div class="banner" @click="handleBannerClick">
			<img class="banner-img" src="../../../../build/logo.png"/>
			<div class="banner-info">
				<div class="banner-title">
					fff
				</div>
				<div class="banner-number">
				<span class="iconfont banner-icon">&#xe692;</span>
				44
				</div>
			</div>
		</div>
		<common-gallary
			:imgs="bannerImgs"
			v-show="showGallary"
			@close="handleGallaryClose">
			
		</common-gallary>
	</div>
</template>

<script>
import CommonGallary from 'common/gallary/Gallary'
export default {
	name: 'DetailBanner',
	components: {
		CommonGallary
	},
	data () {
		return{
			showGallary:false,
			bannerImgs:['http://img1.qunarzz.com/sight/p0/1510/6e/6e4a85e8bc9fcc290.img.jpg_350x240_2736f9ff.jpg','http://img1.qunarzz.com/sight/p0/1510/9c/9c27c8231a5d3e8a90.img.jpg_350x240_e6045463.jpg']
		}
	},
	methods: {
		handleGallaryClose () {
			this.showGallary = false
		},
		handleBannerClick () {
			this.showGallary = true
		}
	}
}
</script>

<style lang="stylus" scoped>
	.banner
		position:relative
		overflow:hidden
		height:0
		padding-bottom:55%
		.banner-img
			width:100%
		.banner-info
			display:flex
			position:absolute
			left:0
			right:0
			bottom:0
			line-height:.6rem
			color:#fff
			background-image:linear-gradient(top,rgba(0,0,0,0),rgba(0, 0, 0, 0.8))
			.banner-title
				flex:1
				font-size:.32rem
				padding:.2rem
			.banner-number
				height:.32rem
				line-height:.32rem
				margin-top:.14rem
				padding:0 .4rem
				border-radius:.2rem
				background:rgba(0, 0, 0, .8)
				font-size:.24rem
				.banner-icon
					font-size:.24rem
</style>
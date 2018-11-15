<template>
<div>
  <div class="banner" @click="handleBannerClick">
  	<img class="banner-img" src="http://img1.qunarzz.com/sight/p0/1409/19/adca619faaab0898245dc4ec482b5722.jpg_600x330_f922b488.jpg" />
  	
  		
  	<div class="banner-info">
        <div class="banner-tittle">
          故宫(AAAAA景区
        </div>
        <div class="banner-number">
          <span class="iconfont banner-icon">&#xe692;</span>
          39
        </div>
    </div>
    
  </div>
  <common-gallary v-show="showGallary" :imgs="imgs" @close="handleGallaryClose" ></common-gallary>
 </div>
</template>

<script>
import CommonGallary from '@/common/gallary/Gallary'
export default {
  name:'DetailBanner',
  data(){
  	return{
  		showGallary:false,
  		imgs:['http://img1.qunarzz.com/sight/p0/1811/2c/2c8c52e607015dd2a3.img.jpg_r_800x800_3ed019ea.jpg','http://img1.qunarzz.com/sight/p0/1811/2c/2c8c52e607015dd2a3.img.jpg_r_800x800_3ed019ea.jpg','http://img1.qunarzz.com/sight/p0/1811/2c/2c8c52e607015dd2a3.img.jpg_r_800x800_3ed019ea.jpg']

  	}
  },
  methods:{
  	handleBannerClick(){
  		this.showGallary = true
  	},
  	handleGallaryClose () {
      this.showGallary = false
    }
  },
  components:{
  	CommonGallary,
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
			background-image: linear-gradient(top, rgba(0, 0, 0, 0), rgba(0, 0, 0, 0.8))
			.banner-tittle
				flex:1
				font-size:.32rem
				padding: 0 .2rem
			.banner-number
				height:.32rem
				padding: 0 .4rem
				margin-top:.14rem
				line-height:.32rem
				border-radius:.2rem
				background:rgba(0,0,0,.8)
				font-size:.24rem
				.banner-icon
					font-size:.24rem
	
</style>

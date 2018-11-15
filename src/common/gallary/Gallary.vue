<template>
	<div class="container" @click="handleGallaryClick">
		<div class="wrapper">
			<swiper :options="swiperOptions">
		        <swiper-slide>
		          <img class="gallary-img" src="http://img1.qunarzz.com/sight/p0/1811/2c/2c8c52e607015dd2a3.img.jpg_r_800x800_3ed019ea.jpg" />
		        </swiper-slide>
		        <swiper-slide>
		          <img class="gallary-img" src="http://img1.qunarzz.com/sight/p0/1811/8a/8a2717e869e3e210a3.img.jpg_r_800x800_8a3fc67f.jpg" />
		        </swiper-slide>
		        <div class="swiper-pagination" slot="pagination"></div>
		     </swiper>
		</div>
	</div>
	

</template>
<script>
	export default	{
		name:'CommonGallary',
		data () {
		    return {
		      swiperOptions: {
		        pagination: '.swiper-pagination',
		        paginationType: 'fraction',
		        observeParents: true,
		        observer: true
		        
		      }
		    }
	  	},
	  	methods: {
		    handleGallaryClick () {
		      this.$emit('close')
		    }
		}
	}
	
	

</script>
<style lang="stylus" scoped>
  .container >>> .swiper-container
   	overflow:inherit
  .container
    display: flex
    flex-direction: column
    justify-content: center
    z-index: 99
    position: fixed
    left: 0
    right: 0
    top: 0
    bottom: 0
    background: #000
    .wrapper
     	
    	height:0
    	width:100%
    	padding-bottom:100%
    	.gallary-img
    		width:100%
    	.swiper-pagination
    		color:#fff
    		bottom:-1rem

      
</style>


<template>
	<div class="wrapper">
	<swiper :options="swiperOption"  v-if="showSwiper">
	    <!-- slides -->
	    <swiper-slide v-for="item of list" :key="item.id"><img class="swiper-img" :src="item.imgUrl"></swiper-slide>
	   
	   
	    <!-- Optional controls -->
	    <div class="swiper-pagination"  slot="pagination"></div>
	    <!--<div class="swiper-button-prev" slot="button-prev"></div>
	    <div class="swiper-button-next" slot="button-next"></div>
	    <div class="swiper-scrollbar"   slot="scrollbar"></div>-->
	 </swiper>
	</div>

  
</template>

<script>
export default {
  name:'HomeSwiper',
  props:{
    list:Array
  },
  data(){
  	return {
  		swiperOption:{
  			pagination:'.swiper-pagination',
  			loop: true
  		},
      swiperList:[{
        "id":"0001",
        "imgUrl":"http://img1.qunarzz.com/piao/fusion/1809/31/da037478f37cf202.jpg_750x200_a02cf862.jpg"
      },{
        "id":"0002",
        "imgUrl":"http://img1.qunarzz.com/piao/fusion/1809/c6/2467595fffc3b302.jpg_750x200_cca13d51.jpg"
      },{
        "id":"0003",
        "imgUrl":"http://img1.qunarzz.com/piao/fusion/1809/ff/1bf7d3a4f6591002.jpg_750x200_40809f2a.jpg"
      },{
        "id":"0004",
        "imgUrl":"http://img1.qunarzz.com/piao/fusion/1809/d4/e298dff35d3af802.jpg_750x200_9b0d56c1.jpg"
      },{
        "id":"0005",
        "imgUrl":"http://img1.qunarzz.com/piao/fusion/1809/31/da037478f37cf202.jpg_750x200_a02cf862.jpg"
      }]
  	}
  } ,
  computed:{
    showSwiper(){
      return this.list.length
    }
  }
}
</script>

<style lang="stylus" scoped>
  .wrapper >>> .swiper-pagination-bullet-active
    	background: #fff
  .wrapper
    	overflow: hidden
    	width: 100%
    	height: 0
    	padding-bottom: 26.25%
    	background: #eee
    	.swiper-img
      		width: 100%

</style>

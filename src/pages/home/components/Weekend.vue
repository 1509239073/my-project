<template>
  <div>
    <div class="title">周末去哪儿</div>
    <ul>
      <li
        class="item border-bottom"
        v-for="item of recommendList"
        :key="item.id"
      >
        <div class="item-img-wrapper">
          <img class="item-img" :src="item.imgUrl" />
        </div>
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.desc}}</p>
        </div>
      </li>
    </ul>
  </div>
</template>
<script>
export default {
  name: 'HomeWeekend', 
  data(){
  	return{
  		recommendList:[{
	        id:'0001',
	        imgUrl:'http://img1.qunarzz.com/sight/source/1509/81/0412da9c4db66a.jpg_r_640x214_8e23871e.jpg',
	        title:'上海杜莎夫人蜡像馆',
	        desc:'11111222233'
	    },{
	        id:'0002',
	        imgUrl:'http://img1.qunarzz.com/sight/source/1509/81/0412da9c4db66a.jpg_r_640x214_8e23871e.jpg',
	        title:'上海杜莎夫人蜡像馆',
	        desc:'11111222233'
	    },{
	        id:'0003',
	        imgUrl:'http://img1.qunarzz.com/sight/source/1509/81/0412da9c4db66a.jpg_r_640x214_8e23871e.jpg',
	        title:'上海杜莎夫人蜡像馆',
	        desc:'111112222333333'
	    }]
  	}
  }
}
</script>
<style lang="stylus" scpoed>
	@import '~styles/mixins.styl'
	.title
		line-height: .4rem
		background:#eee
		text-indent:.2rem
		margin-top:.2rem
	.item-img-wrapper	
		overflow:hidden
		height:0
		padding-bottom:33.9%
		.item-img
			width:100%
	.item-info
		flex:1
		padding:.1rem
		min-width:0
		.item-title
			line-height:.54rem
			font-size:.32rem
			ellipsis()
		.item-desc
			line-height:.4rem
			color:#ccc
			ellipsis()
		.item-button
			background:#ff9300
			padding:0 .2rem
			border-radius: .06rem
			margin-top:.16rem
			line-height:.44rem
	
</style>s

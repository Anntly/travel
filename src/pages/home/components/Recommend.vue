<template>
  <div>
    <div class="title">热销推荐</div>
    <ul>
        <router-link tag="li" :to="'/detail/' + item.id"
        class="item border-bottom" 
        v-for="item of list" 
        :key="item.id">
            <img class="item-img" :src="item.imgUrl">
          <div class="item-info">
            <p class="item-title">{{item.title}}</p>
            <p class="item-desc">{{item.desc}}</p>
            <button class="item-button">查看详情</button>
          </div>
        </router-link>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HomeRecommend',
  props: {
    list: Array
  },
  data(){
    return {

    }
  }
}
</script>

<style lang="stylus" scoped>
  @import '~styles/minxins.styl';
  .title
    margin-top: .2 rem
    line-height: .8 rem
    background: #ccc
    text-align: .2 rem
  .item
    overflow: hidden
    display: flex
    height: 1.9 rem
    .item-img
      width: 1.7 rem
      height: 1.7 rem
      padding: .1 rem
    .item-info
      flex: 1
      padding: .1 rem
      min-width: 0
      .item-title
        line-height: .54 rem
        font-size: .32 rem
        ellipsis()
      .item-desc
        line-height: .4 rem
        color: #ccc
        ellipsis()
      .item-button
        line-height: .44 rem
        margin-top: .16 rem
        background: #ff9300
        padding: 0 .2 rem
        border-radius: .06 rem
        color: #fff
</style>

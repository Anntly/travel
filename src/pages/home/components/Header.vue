<template>
  <div>
    <div class="header">
      <div class="header-left">
        <div class="iconfont back-icon">&#xe624;</div>
      </div>
      <div class="header-input">
        <span class="iconfont">&#xe632;</span> 输入城市/景点/游玩主题
      </div>
      <router-link to="/city">
        <div class="header-right">
          {{this.city}}
          <span class="iconfont arrow-icon">&#xe62d;</span>
        </div>
      </router-link>
    </div>
  </div>
</template>

<script>
  import { mapState } from 'vuex';
  export default {
    name: 'HomeHeader',
    computed: {
    ...mapState(['city']),
    //...mapGetters(['doubleCity'])
  }
  };
  
</script>

<!--@代表的是src目录  style中要使用~@-->
<style lang="stylus" scoped>
  @import '~styles/varibles.styl';
  .header
    display: flex
    line-height: $headerHeight
    background: $bgColor
    color: #fff
    .header-left 
      width: .64 rem
      float: left 
      .back-icon
        text-align: center
        font-size: .4 rem
    .header-input
      flex: 1
      height: .64 rem
      line-height: .64 rem
      margin-top: .12 rem
      margin-left: .2 rem
      padding-left: .1 rem
      background: #fff
      border-radius: .1 rem
      color: #ccc
    .header-right
      min-width: 1.04 rem
      padding: 0 .1rem
      float: right 
      text-align: center
      color: #fff
      .arrow-icon
        margin-left: -.04 rem
        font-size: .24 rem
</style>


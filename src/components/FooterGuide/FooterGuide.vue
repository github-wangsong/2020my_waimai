<template>
  <div>
    <footer class="footer_guide">
      <span class='guide_item ' :class='{on: $route.path==="/msite"}' @click='goto("/msite")'>
        <span>
          <i class="iconfont icon-waimai"></i>
        </span>
        <span>外卖</span>
      </span>
      <span class='guide_item' :class='{on: $route.path==="/search"}' @click='goto("/search")'>
        <span>
          <i class="iconfont icon-search"></i>
        </span>
        <span>搜索</span>
      </span>
      <span class='guide_item' :class='{on: $route.path==="/order"}' @click='goto("/order")'>
        <span>
          <i class="iconfont icon-dingdan"></i>
        </span>
        <span>订单</span>
      </span>
      <span class='guide_item' :class='{on: $route.path==="/profile"}' @click='goto("/profile")'>
        <span>
          <i class="iconfont icon-geren"></i>
        </span>
        <span>我的</span>
      </span>
    </footer>
  </div>
</template>

<script>
  export default {
    methods: {
      goto: function(path) {
        this.$router.replace(path)
      }
    }
  }
</script>

<style lang="stylus" rel="stylesheet/stylus" scoped>
  @import "../../common/stylus/mixins.styl"
  .footer_guide
    top-border-1px(#ccc)
    z-index 100
    display flex
    position fixed
    // justify-content space-around
    left 0
    bottom 0
    width 100%
    height 50px
    background-color #fff
    .guide_item
      display flex
      flex-flow column 
      text-align center
      // width 25%
      flex 1
      &.on
        color $green
      span 
        margin-top 4px
        font-size 12px
        .iconfont
          font-size 22px      



</style>

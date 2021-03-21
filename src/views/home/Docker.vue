<!--  -->
<template>
  <div class="docker">
    <div v-for="(item,index) in dockerList" :key="item.icon"
    :class="{'docker_tiem': true, 'docker_item-active': index === 0}"
    class="docker_item">
      <div class="iconfont" v-html="item.icon" />
      <div class="docker_title">{{item.text}}</div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Docker',
  data () {
    return {
      dockerList: [
        { icon: '&#xe603;', text: '首页' },
        { icon: '&#xe611;', text: '购物车' },
        { icon: '&#xe608;', text: '订单' },
        { icon: '&#xe610;', text: '我的' }
      ]
    }
  }
}
</script>
<style lang="scss" scoped>
/* @import url(); 引入css类 */
@import "../../style/viriables.scss";
@import "../../style/mixins.scss";
.docker {
  display: flex;
  box-sizing: border-box;
  position: absolute;
  padding: 0 0.18rem;
  left: 0;
  bottom: 0;
  width: 100%;
  height: 0.49rem;
  border-top: 1px solid $content-bgcolor;
  color: $content-fontcolor;
  &_item {
    flex: 1;
    text-align: center;
    .iconfont {
      margin: 0.07rem 0 0.02rem 0;
      font-size: 0.18rem;
    }
    &-active {
      color: #1fa4fc;
    }
  }
  &_title {
    font-size: 0.2rem;
    transform: scale(0.5, 0.5);
    transform-origin: center top;
  }
}
</style>

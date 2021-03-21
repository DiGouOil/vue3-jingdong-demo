<!--  -->
<template>
  <div class="nearby">
    <h3 class="nearby_title">附近店铺</h3>
    <div class="nearby_item" v-for="item in nearbyList" :key="item.id">
      <img
        class="nearby_item_img"
        :src="item.imgUrl"
        alt=""
      />
      <div class="nearby_item_content">
        <div class="nearby_item_content_title">{{item.title}}</div>
        <div class="nearby_item_content_tags">
          <span class="nearby_item_content_tag"
          v-for="(innerItem,innerIndex) in item.tags" :key="innerIndex">{{innerItem}}</span>
        </div>
        <p class="nearby_item_content_highlight">
          {{item.desc}}
        </p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Nearby',
  data () {
    return {
      nearbyList: [{
        id: 1,
        imgUrl: 'http://www.dell-lee.com/imgs/vue3/near.png',
        title: '沃尔玛',
        tags: ['月售1万+', '起送￥0', '急促运费￥5'],
        desc: 'VIP尊享满89元减4元运费卷（每月3张）'
      }, {
        id: 2,
        imgUrl: 'http://www.dell-lee.com/imgs/vue3/near.png',
        title: '沃尔玛',
        tags: ['月售1万+', '起送￥0', '急促运费￥5'],
        desc: 'VIP尊享满89元减4元运费卷（每月3张）'
      }]
    }
  }
}
</script>
<style lang="scss" scoped>
/* @import url(); 引入css类 */
@import "../../style/viriables.scss";
@import "../../style/mixins.scss";
.nearby {
  &_title {
    margin: 0.16rem 0 0.02rem 0;
    font-size: 0.18rem;
    font-weight: normal;
    color: $content-fontcolor;
  }
  &_item {
    display: flex;
    padding-top: 0.12rem;
    &_img {
      margin-right: 0.16rem;
      width: 0.56rem;
      height: 0.56rem;
    }
    &_content {
      padding-bottom: 0.12rem;
      border-bottom: 1px solid $content-bgcolor;
      flex: 1;
      &_title {
        line-height: 0.22rem;
        font-size: 0.16rem;
        color: $content-fontcolor;
      }
      &_tags {
        margin-top: 0.08rem;
        line-height: 0.18rem;
        font-size: 0.13rem;
        color: $content-fontcolor;
      }
      &_tag {
        margin-right: 0.16rem;
      }
      &_highlight {
        color: #e93b3b;
        line-height: 0.18rem;
        font-size: 0.13rem;
        margin: 0.08rem 0 0 0;
      }
    }
  }
}
</style>

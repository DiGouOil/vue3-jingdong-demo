<!--  -->
<template>
    <div class="position">
      <span class="iconfont position_icon">&#xe70b;</span>
        北京理工大学国防科技园2号楼10层
      <span class="iconfont position_notice">&#xe860;</span>
    </div>
    <div class="search">
      <span class="iconfont">&#xe665;</span>
      <span class="serch_text">山姆会员商店优惠产品</span>
    </div>
    <div class="banner">
      <img class="banner_img" src="http://www.dell-lee.com/imgs/vue3/banner.jpg" alt="">
    </div>
    <div class="icons">
      <div class="icons_item" v-for="(item,index) in iconList" :key="index">
        <img class="icons_item_img" :src="`http://www.dell-lee.com/imgs/vue3/${item.imgName}.png`" alt=""/>
        <p class="icons_item_desc">{{item.desc}}</p>
      </div>
    </div>
    <div class="gap"></div>
</template>

<script>
export default {
  name: 'StaticPart',
  data () {
    return {
      iconList: [
        { imgName: '超市', desc: '超市便利' },
        { imgName: '菜市场', desc: '菜市场' },
        { imgName: '水果店', desc: '水果店' },
        { imgName: '鲜花', desc: '鲜花绿植' },
        { imgName: '医药健康', desc: '医药健康' },
        { imgName: '家居', desc: '家居时尚' },
        { imgName: '蛋糕', desc: '烘焙蛋糕' },
        { imgName: '签到', desc: '签到' },
        { imgName: '大牌免运', desc: '大牌免运' },
        { imgName: '红包', desc: '红包套餐' }
      ]
    }
  }
}
</script>
<style lang="scss" scoped>
/* @import url(); 引入css类 */
@import '../../style/viriables.scss';
@import '../../style/mixins.scss';
.position{
  position: relative;
  padding:0.16rem 0.24rem 0.16rem 0;
  line-height: 0.22rem;
  font-size: 0.16rem;
  color: $content-fontcolor;
  @include ellipsis;
  .position_icon{
    position: relative;
    top:0.01rem;
    font-size: 0.2rem;
  }
  .position_notice{
    position: absolute;
    right: 0;
    top: 0.17rem;
    font-size: 0.2rem;
  }
}
.search{
  margin-bottom: 0.12rem;
  line-height: 0.32rem;
  background: #f5f5f5;
  color:#B7B7B7;
  border-radius: 0.16rem;
  .iconfont{
    position: relative;
    top:0.01rem;
    padding: 0 0.12rem 0 0.16rem;
    font-size: 0.16rem;
  }
  &_text{
    display: inline-block;
    font-size: 0.14rem;
  }
}
.banner{
  height: 0;
  overflow: hidden;
  padding-bottom: 25.4%;
  &_img{
    width: 100%;
  }
}
.icons{
  display: flex;
  flex-wrap: wrap;
  margin-top: 0.16rem;
  &_item{
    width: 20%;
    &_img{
      display: block;
      width: 0.4rem;
      height: 0.4rem;
      margin: 0 auto;
    }
    &_desc{
      color: $content-fontcolor;
      text-align: center;
      margin: 0.06rem 0 0.16rem 0;
    }
  }
}
.gap{
  margin: 0 -0.18rem;
  height: 0.1rem;
  background: $content-bgcolor;
}
</style>

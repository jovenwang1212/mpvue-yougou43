<template>
  <div>
    <div class="header">
      <div class="inner">
        <icon type="search"
              size="16">
        </icon>
        <span>搜索</span>
      </div>
    </div>
    <!-- 轮播图 -->
    <swiper indicator-dots
            circular autoplay indicator-color="rgba(255,255,255,0.3)" indicator-active-color="#fff">
      <block v-for="(item, index) in 3"
             :key="index">
        <swiper-item>
          <image src="https://api.zbztb.cn/pyg/banner1.png"></image>
        </swiper-item>
      </block>
    </swiper>
    <!-- 导航 -->
    <div class="nav">
      <img v-for="(item, index) in 4"
           :key="index"
           src="https://api.zbztb.cn/pyg/icon_index_nav_4@2x.png"
           alt="">
    </div>
    <!-- 楼层 -->
    <ul>
      <li class="floor"
          v-for="(floor, i) in 3"
          :key="i">
        <img src="https://api.zbztb.cn/pyg/pic_floor01_title.png"
             alt="">
        <div class="product_list">
          <img src="https://api.zbztb.cn/pyg/pic_floor01_1@2x.png"
               alt="">
          <div class="right">
            <img v-for="(item, index) in 4"
                 :key="index"
                 src="https://api.zbztb.cn/pyg/pic_floor01_2@2x.png"
                 alt="">
          </div>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {

}
</script>

<style lang="less">
.header {
  height: 100rpx;
  background-color: #eb4450;
  padding: 20rpx 16rpx;
  box-sizing: border-box;
  .inner {
    background-color: #fff;
    border-radius: 4rpx;
    height: 60rpx;
    color: #bbb;
    display: flex;
    align-items: center;
    justify-content: center;
    icon {
      margin: 6rpx 16rpx 0 0;
    }
  }
}
swiper {
  height: 340rpx;
  image {
    width: 100%;
    height: 340rpx;
  }
}

.nav {
  display: flex;
  height: 194rpx;
  justify-content: space-around;
  align-items: center;
  img {
    width: 128rpx;
    height: 140rpx;
  }
}
.floor {
  padding:20rpx 17rpx 0;
  > img {
    height: 88rpx;
    width: 100%;
  }
}

.product_list {
  display: flex;
  > img {
    width: 232rpx;
    height: 386rpx;
  }
  .right {
    flex:1;
    font-size: 0;
    > img {
      width: 232rpx;
      height: 188rpx;
      margin:0 0 10rpx 10rpx;
    }
  }
}
</style>
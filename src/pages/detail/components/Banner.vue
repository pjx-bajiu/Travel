<template>
  <div>
    <div class="banner" @click="handleBannerClick">
      <img class="banner-img" src="../../../assets/styles/images/cat.jpg" />
      <div class="banner-info">
        <div class="banner-title">大连海洋世界（AAAA）景区</div>
        <div class="banner-number">
          <span class="iconfont banner-icon">&#xe8d3;</span>
          39
        </div>
      </div>
    </div>
    <common-gallary :imgs="imgs" v-show="showGallary" @close="handleGallaryClick">

    </common-gallary>
  </div>
</template>

<script>
import CommonGallary from "common/gallary/Gallary.vue";
export default {
  name: "DetailBanner",
  data () {
    return {
      showGallary:false,
      imgs:[require('../../../assets/styles/images/cat.jpg'),require('../../../assets/styles/images/cat.jpg')]
    }
  },
  methods: {
    handleBannerClick () {
      this.showGallary = true;
    },
    handleGallaryClick() {
      this.showGallary = false;
    }
  },
  components: {
    CommonGallary,
  },
};
</script>

<style lang='stylus' scoped>
.banner {
  position: relative;
  overflow: hidden;
  height: 0;
  padding-bottom: 55%;

  .banner-img {
    width: 100%;
  }

  .banner-info {
    display: flex;
    position: absolute;
    left: 0;
    right: 0;
    bottom: 0;
    line-height: 0.6rem;
    color: #fff;
    background-image: linear-gradient(top, rgba(0, 0, 0, 0), rgba(0, 0, 0, 0.8));

    .banner-title {
      flex: 1;
      font-size: 0.32rem;
      padding: 0 0.2rem;
    }

    .banner-number {
      line-height: 0.32rem;
      height: 0.32rem;
      padding: 0 0.4rem;
      margin-top: 0.14rem;
      border-radius: 0.2rem;
      background: rgba(0, 0, 0, 0.8);
      font-size: 0.24rem;

      .banner-icon {
        font-size: 0.24rem;
      }
    }
  }
}
</style>
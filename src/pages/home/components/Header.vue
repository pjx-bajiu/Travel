<template>
  <div class="header">
    <div class="header-left">
      <div class="iconfont back-icon">&#xe624;</div>
    </div>
    <div class="header-input">
      <span class="iconfont">&#xe632;</span>
      输入城市/景点/游玩/主题/徐海强
    </div>
    <div class="header-right">
      {{this.city}}
      <span class="iconfont arrow-icon">&#xe600;</span>
    </div>
  </div>
</template>

<script>
export default {
  name: "HomeHeader",
  props: {
    city: String
  }
};
</script>

<style lang="stylus" scoped>
@import '~styles/varibles.styl'
.header {
  display: flex;
  line-height: 0.86rem;
  background: $bgColor;
  color: #fff;

  .header-left {
    width: 0.64rem;
    float: left;
    text-align: center;

    .back-icon {
      font-size: 0.4rem;
    }
  }

  .header-input {
    flex: 1;
    margin-top: 0.12rem;
    height: 0.64rem;
    line-height: 0.64rem;
    padding-left: 0.2rem;
    margin-left: 0.2rem;
    background: #fff;
    border-radius: 0.1rem;
    color: #ccc;
  }

  .header-right {
    width: 1.24rem;
    float: right;
    line-height: 0.86rem;
    text-align: center;

    .arrow-icon {
      margin-left: -0.05rem;
      font-size: 0.24rem;
    }
  }
}
</style>

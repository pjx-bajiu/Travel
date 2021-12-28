<template>
  <div>
    <div class="title">周末去哪儿</div>
    <ul>
      <li class="weekend-all border-botttom" v-for="item of list" :key="item.id">
        <div class="weekend-img-wrapper"><img :src="item.imgUrl" class="weekend-img" /></div>
        <div class="weekend-title">
          <p class="weekend-title-one">{{ item.title }}</p>
          <p class="weekend-title-two">{{ item.desc }}</p>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "HomeWeekend",
  props: {
    list: Array
  }
};
</script>

<style lang='stylus' scoped>
@import '~styles/minxins.styl';

.title {
  line-height: 0.8rem;
  text-indent: 0.2rem;
  background: #eee;
}

.weekend-all {
  .weekend-img-wrapper {
      overflow: hidden;
      height: 0;
      padding-bottom: 37.09%;
  }
  .weekend-img {
    width: 100%;
  }

  .weekend-title {
    padding: .1rem 0;
    line-height: 0.4rem;
    text-indent: 0.2rem;

    .weekend-title-two {
      ellipsis();
      font-size: 0.1rem;
      color: #aaa;
    }
  }
}
</style>
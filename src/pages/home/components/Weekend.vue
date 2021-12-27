<template>
  <div>
    <div class="title">周末去哪儿</div>
    <ul>
      <li class="weekend-all border-botttom" v-for="item of WeekendList" :key="item.id">
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
  data() {
    return {
      WeekendList: [
        {
          id: "0001",
          imgUrl: require("../../../assets/styles/images/focus1.jpg"),
          title: "温泉水上乐园",
          desc: "泡泡温泉，吹吹海风，深觉人间美好",
        },
        {
          id: "0002",
          imgUrl: require("../../../assets/styles/images/focus.jpg"),
          title: "温泉水上乐园",
          desc: "泡泡温泉，吹吹海风，深觉人间美好",
        },
        {
          id: "0003",
          imgUrl: require("../../../assets/styles/images/focus1.jpg"),
          title: "温泉水上乐园",
          desc: "泡泡温泉，吹吹海风，深觉人间美好,泡泡温泉，吹吹海风，深觉人间美好,泡泡温泉，吹吹海风，深觉人间美好,泡泡温泉，吹吹海风，深觉人间美好",
        },
        {
          id: "0004",
          imgUrl: require("../../../assets/styles/images/focus.jpg"),
          title: "温泉水上乐园",
          desc: "泡泡温泉，吹吹海风，深觉人间美好",
        },
      ],
    };
  },
};
</script>

<style lang='stylus' scoped>
@import '~styles/minxins.styl';

.title {
  margin-top: 0.1rem;
  line-height: 0.8rem;
  text-indent: 0.2rem;
  background: #eee;
}

.weekend-all {
  .weekend-img-wrapper {
      overflow: hidden;
      height: 0;
      padding-bottom: 31.9%;
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
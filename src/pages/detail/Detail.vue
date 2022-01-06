<template>
  <div>
    <detail-banner></detail-banner>
    <detail-header></detail-header>
    <div class="content">
      <detail-list :list="list"></detail-list>
    </div>
  </div>
</template>

<script>
import DetailBanner from "./components/Banner.vue";
import DetailHeader from "./components/Header.vue";
import DetailList from "./components/List.vue";
export default {
  name: "Detail",
  components: {
    DetailBanner,
    DetailHeader,
    DetailList,
  },
  data() {
    return {
      list: [
        {
          title: "成人票",
          children: [
            {
              title: "【春节优惠】大连圣亚海洋世界五馆单人票",
              children: [
                {
                  title: "含海洋世界+珊瑚世界+极低世界+深海世界+游玩世界",
                },
              ],
            },
            {
              title: "成人五馆联票",
            },
          ],
        },
        {
          title: "学生票",
        },
        {
          title: "儿童票",
        },
        {
          title: "特惠票",
        },
      ],
    };
  },
};
</script>

<style lang='stylus' scoped>
.content {
  height: 50rem;
}
</style>
<template>
  <div>
    <div class="item" v-for="(item, index) of list" :key="index">
      <div class="item-title border-bottom">
          <span v-if="item.id" class="item-title-icon"></span>
          <span :class="{'other-level': !item.id}">{{item.title}}</span>
      </div>
      <div v-if="item.children" class="item-children">
          <detail-list :list="item.children"></detail-list>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "DetailList",
  props: {
    list: Array,
  },
};
</script>

<style lang='stylus' scoped>
.item-title {
    line-height: .8rem;
    font-size: .32rem;
    padding: 0 .2rem;
    .item-title-icon {
        position: relative;
        left: .06rem;
        top: .06rem;
        display: inline-block;
        width: .36rem;
        height: .36rem;
        margin-right: .1rem;
        background: url('../../../assets/styles/images/icon.png') 0 -.45rem no-repeat;
        background-size: .4rem 3rem;
    }
    .other-level {
        font-size: 0.24rem;
    }
}
.item-children {
    padding: 0 .2rem;
    overflow: hidden;
    white-space: nowrap;
    text-overflow: ellipsis;
    font-size: .24rem;
}
</style>
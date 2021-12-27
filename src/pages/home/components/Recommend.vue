<template>
  <div>
    <div class="title">热销推荐</div>
    <ul class="item-margin">
      <li class="item border-botttom" v-for='item of recommendList' :key='item.id'>
        <img class="item-img" :src="item.imgUrl" />
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.desc}}</p>
          <button class="item-button">查看详情</button>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "HomeRcommend",
  data () {
      return {
          recommendList: [{
          id:'0001',
          imgUrl: require('../../../assets/styles/images/cat.jpg'),
          title:'猫咖',
          desc:'60元畅游2小时,60元畅游2小时,60元畅游2小时.60元畅游2小时'
      },
      {
          id:'0002',
          imgUrl: require('../../../assets/styles/images/cat.jpg'),
          title:'猫咖',
          desc:'60元畅游2小时,60元畅游2小时,60元畅游2小时.60元畅游2小时'
      },
      {
          id:'0003',
          imgUrl: require('../../../assets/styles/images/cat.jpg'),
          title:'猫咖',
          desc:'60元畅游2小时,60元畅游2小时,60元畅游2小时.60元畅游2小时'
      },
      {
          id:'0004',
          imgUrl: require('../../../assets/styles/images/cat.jpg'),
          title:'猫咖',
          desc:'60元畅游2小时,60元畅游2小时,60元畅游2小时.60元畅游2小时'
      }]
      }
  }
};
</script>

<style lang='stylus' scope>
@import '~styles/minxins.styl'
.title {
  margin-top: 0.2rem;
  line-height: 0.8rem;
  background: #eee;
  text-indent: 0.2rem;
}
.item-margin {
    margin-top: .1rem;
    margin-left: .08rem;
}
.item {
    display: flex;
    height: 1.9rem;
    &-img {
        width: 1.7rem;
        height: 1.7rem;
        padding: .1rem;
    }
    &-info {
        flex: 1;
        padding: .1rem;
        min-width: 0;
        .item-title {
            line-height: .54rem;
            font-size: .32rem;
            ellipsis();
        }
        .item-desc {
            line-height: .4rem;
            color: #ccc;
            ellipsis();
        }
        .item-button {
            line-height: .44rem
            margin-top: .16rem;
            background: #ff9300;
            padding: 0 .2rem;
            border-radius: .06rem;
            color: #fff
        }
    }
}
</style>  
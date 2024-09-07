<template>
  <div class="container">
    <u-sticky bgColor="#fff">
      <u-tabs :list="list1" :current="currentTab" class="tabs-center" @change="handleTabChange"></u-tabs>
    </u-sticky>

    <swiper :current="currentTab" @change="swiperChange" class="tab-content">
      <swiper-item>
        <Test01/>
      </swiper-item>
      <swiper-item>
        <!--        可以给Test02 传入message 参数-->
        <Test02/>
      </swiper-item>
      <swiper-item>
        <Test03/>
      </swiper-item>
    </swiper>
  </div>
</template>

<script>
import Test01 from "../test-tabs/Test01.vue";
import Test02 from "../test-tabs/Test02.vue";
import Test03 from "../test-tabs/Test03.vue";

export default {
  components: {
    Test01,
    Test02,
    Test03
  },
  data() {
    return {
      list1: [
        {name: '关注'},
        {name: '推荐'},
        {name: '电影'}
      ],
      currentTab: 0  // 当前选中的 tab 索引
    };
  },
  methods: {
    // 点击 tabs 时触发，更新 currentTab
    handleTabChange(e) {
      this.currentTab = e.index;
    },

    // swiper 滑动时触发，更新 tabs 选中状态
    swiperChange(event) {
      this.currentTab = event.detail.current;
    }
  }
}
</script>

<style>
.container {
  display: flex;
  flex-direction: column;
  align-items: center;
}

.tabs-center {
  display: flex;
  justify-content: center;
  width: 100%;
}

.tab-content {
  width: 100%;
  height: 88vh; /* 设置内容区域的高度 */
}
</style>

<template>
  <!-- 主页开始 -->
  <div class="index">
    <!-- 右上角时间 -->
    <span class="time">时间</span>
    <!-- 时间结束 -->
    <!-- 福利入口 -->
    <span class="fuli">
      <router-link to="javascript:;">
        <img src="../assets/image/fuli.png" alt />
      </router-link>
    </span>
    <!-- 福利结束 -->
    <!-- 轮播区域 -->
    <div class="lunbo">
      <mt-swipe :auto="4000">
        <mt-swipe-item>
          <img src="../assets/image/lunbo1.png" alt />
        </mt-swipe-item>
        <mt-swipe-item>
          <img src="../assets/image/lunbo2.png" alt />
        </mt-swipe-item>
        <mt-swipe-item>
          <img src="../assets/image/lunbo3.png" alt />
        </mt-swipe-item>
      </mt-swipe>
    </div>
    <!-- 轮播结束 -->
    <!-- 选项卡开始  -->
    <div class="go">
      <mt-navbar v-model="active">
        <mt-tab-item id="1">
          <img src="../assets/image/yusheng.png" sloat="icon" />
          雨声
        </mt-tab-item>
        <mt-tab-item id="2">
          <img src="../assets/image/zhuanzhu.png" sloat="icon" />
          专注
        </mt-tab-item>
        <mt-tab-item id="3">
          <img src="../assets/image/mingxiang.png" sloat="icon" />
          冥想
        </mt-tab-item>
        <mt-tab-item id="4">
          <img src="../assets/image/jianya.png" sloat="icon" />
          减压
        </mt-tab-item>
        <mt-tab-item id="5">
          <img src="../assets/image/jieyou.png" sloat="icon" />
          解忧
        </mt-tab-item>
      </mt-navbar>
    </div>
    <!-- 选项卡结束 -->
    <!-- 助眠声音开始 -->
    <div class="life">
      <span class="life-title">助眠声音</span>
      <span class="life-more">
        <router-link to="../views/About.vue">更多</router-link>
      </span>
      <mt-navbar>
        <mt-tab-item id="1">
          <router-link to="http://www.baidu.com">
            <img src="../assets/image/主页板块测试图.jpg" sloat="icon" title />
            <span class="letter">夏日光彩</span>
          </router-link>
        </mt-tab-item>
        <mt-tab-item id="2">
          <router-link to="javascript:;">
            <img src="../assets/image/主页板块测试图.jpg" sloat="icon" />
            <span class="letter">轻柔洗头</span>
          </router-link>
        </mt-tab-item>
        <mt-tab-item id="3">
          <router-link to="javascript:;">
            <img src="../assets/image/主页板块测试图.jpg" sloat="icon" />
            <span class="letter">冬雨苍凉</span>
          </router-link>
        </mt-tab-item>
      </mt-navbar>
    </div>
    <!-- 助眠声音结束 -->
    <!-- 冥想时刻 -->
    <div class="life mt">
      <span class="life-title">冥想时刻</span>
      <span class="life-more">更多</span>
      <mt-navbar>
        <mt-tab-item id="1">
          <img src="../assets/image/主页板块测试图.jpg" sloat="icon" title />
          <span class="letter">青青草地</span>
        </mt-tab-item>
        <mt-tab-item id="2">
          <img src="../assets/image/主页板块测试图.jpg" sloat="icon" />
          <span class="letter">阵雨绵绵</span>
        </mt-tab-item>
        <mt-tab-item id="3">
          <img src="../assets/image/主页板块测试图.jpg" sloat="icon" />
          <span class="letter">舒缓紧张</span>
        </mt-tab-item>
      </mt-navbar>
    </div>
    <!-- 冥想时刻结束 -->
    <!-- 心理测评 -->
    <div class="ceping">
      <span class="ceping-title">心理测评</span>
      <label>
        <router-link to="javascript:;">更多</router-link>
      </label>
    </div>
    <!-- 心理测评结束 -->
    <!-- 减压视频 -->
    <div class="life mt">
      <span class="life-title">减压视频</span>
      <span class="life-more">更多</span>
      <mt-navbar>
        <mt-tab-item id="1">
          <img src="../assets/image/主页板块测试图.jpg" sloot="icon" title />
          <span class="letter">杏雨梨云</span>
        </mt-tab-item>
        <mt-tab-item id="2">
          <img src="../assets/image/主页板块测试图.jpg" sloot="icon" />
          <span class="letter">爱的旅程</span>
        </mt-tab-item>
        <mt-tab-item id="3">
          <img src="../assets/image/主页板块测试图.jpg" sloot="icon" />
          <span class="letter">午餐邂逅</span>
        </mt-tab-item>
      </mt-navbar>
      <span class="more_tab">暂时没有更多了</span>
    </div>
    <!-- 减压视频结束 -->
    <!-- 底部选项卡 -->
    <mt-tabbar v-model="selectedTab" fixed class="tab">
      <mt-tab-item id="home">
        <router-link to="/">首页</router-link>
        <img src="../assets/home_red.png" slot="icon" v-if="selectedTab == 'home'" />
        <img src="../assets/home_gray.png" slot="icon" v-else />
      </mt-tab-item>
      <mt-tab-item id="sound">
        <router-link to="sound">声音</router-link>
        <img src="../assets/sound_gray.png" slot="icon" v-if="selectedTab == 'sound'" />
        <img src="../assets/sound_red.png" slot="icon" v-else />
      </mt-tab-item>
      <mt-tab-item id="focus">
        <router-link to="focus">专注</router-link>
        <img src="../assets/focus_gray.png" slot="icon" v-if="selectedTab == 'focus'" />
        <img src="../assets/focus_red.png" slot="icon" v-else />
      </mt-tab-item>
      <mt-tab-item id="me">
        <router-link to="me">我的</router-link>
        <img src="../assets/me_gary.png" alt slot="icon" v-if="selecedTab == 'me'" />
        <img src="../assets/me_red.png" alt slot="icon" v-else />
      </mt-tab-item>
    </mt-tabbar>
    <!-- 底部选项卡结束 -->
  </div>
  <!-- 主页结束 -->
</template>

<script>
export default {
  data() {
    return {
      n: "",
      active: 1,
      //默认被选定的底部选项卡
      selectedTab: "home",
    };
  },
  methods: {
    watch: {
      //监听顶部选项卡的变化
      active() {
        //切换顶部选项卡时,清空之前存储的文章数据
        this.articles = [];
        //切换顶部选项卡时,页码初始值为1
        this.page = 1;
        //加载数据
        this.loadData();
      },
      //监听底部选项卡的变化
      selectedTab() {
        switch (this.selectedTab) {
          case "home":
            this.$router.push("/");
            break;
          case "cart":
            this.$router.push("/list");
            break;
          case "center":
            this.$router.push("/navbar");
            break;
        }
      },
    },
  },
};
</script>
<style scope>
.more_tab {
  display: inline-block;
  margin-top: 1rem;
}
/* 测评 */

/* 板块所有 */
/* 板块上边距 */
.mt {
  margin-top: -0.7rem;
  margin-bottom: 5rem;
}

/* 助眠区 */
/*助眠更多*/
.life-more {
  position: relative;
  top: 1.6rem;
  left: 6.7rem;
  font-size: 0.8rem;
}

/* 助眠小标题 */
.life .letter {
  margin-right: 2rem;
  font-size: 13px;
}

/* 助眠大标题 */
.life-title {
  font-size: 22px;
  font-weight: bolder;
  color: black;
  position: relative;
  top: 1.7rem;
  right: 6.7rem;
  z-index: 999;
}

/* 板块中的上下内边距和左右内边距 */
.life .mint-navbar .mint-tab-item {
  padding: 32px 8px 7px;
  font-size: 15px;
}

/* 板块中图片的宽度百分百 */
.life img {
  width: 100%;
}

/* 助眠板块的选中样式取消自带的下边框和下外边距 */
.life .mint-navbar .mint-tab-item.is-selected {
  /* border-bottom: 3px solid #26a2ff; */
  color: #333333cf !important;
  margin-top: 27px !important;
}

/* 助眠选项卡字体大小 行高 */
.life .mint-tab-item-label {
  color: inherit;
  font-size: 16px;
  line-height: 1;
}

/* 选项卡样式 */
/*更改字体大小14px 字体颜色#3333333cf 行高为1.6*/
.go .mint-tab-item-label {
  color: #333333cf !important;
  font-size: 14px;
  line-height: 1.6;
}

/* 更改每个单选的上下内边距和左右内边距 */
.go .mint-navbar .mint-tab-item {
  padding: 10px 11px !important;
}

/* 轮播图样式 */
/* 调整轮播容器的高度 */
.mint-swipe,
.mint-swipe-items-wrap {
  height: 10rem !important;
}

/* 调整轮播图片的边框倒角和宽度 */
.mint-swipe,
.mint-swipe-items-wrap img {
  border-radius: 6px;
  width: 100%;
}

/* 调整分页指示器的选中颜色 */
.mint-swipe-indicator.is-active {
  background: red !important;
}

/* 调整分页指示器的位置靠上一点 */
.mint-swipe-indicators {
  bottom: 21px !important;
}

/* 时间样式 */
/* 时间左浮并往下走0.1rem 字重为bolder 大小为26px */
.time {
  font-weight: bolder;
  font-size: 26px;
  float: left;
  margin: 1rem;
}

/* 福利 */
/* 福利图标右浮并往上走0.6rem */
.fuli {
  float: right;
  margin: 1rem;
}
.tab {
  margin-top: 2rem;
}

.index {
  text-align: center;
}
/**{
  text-align: center !important;
}*/
.mint-tabbar > .mint-tab-item.is-selected {
  /* background-color: #eaeaea; */
  color: #26a2ff;
}
</style>
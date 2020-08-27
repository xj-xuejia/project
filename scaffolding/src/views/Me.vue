<template>
  <div>
    <!-- 顶部 -->
    <div class="top">
      <div class="topw">我的</div>
    </div>
    <div class="zynr">
      <div class="loginw">
        <!--<img src alt />-->
        <a href="/login">点击登录</a>
      </div>
      <!-- 选项卡 -->
      <mt-navbar v-model="active" id="go">
        <mt-tab-item id="1">
          <img src="../assets/myselect.png" sloat="icon" />
          <br />收藏
        </mt-tab-item>
        <mt-tab-item id="2">
          <img src="../assets/mydownload.png" sloat="icon" />
          <br />下载
        </mt-tab-item>
        <mt-tab-item id="3">
          <img src="../assets/myblog.png" sloat="icon" />
          <br />消息
        </mt-tab-item>
        <mt-tab-item id="4">
          <img src="../assets/moresettings.png" sloat="icon" />
          <br />设置
        </mt-tab-item>
      </mt-navbar>
      <!-- 昨日睡眠 -->
      <div class="nrit">
        <div class="nritwz">昨日睡眠</div>
        <div class="nritsj1">
          <div class="nritsj11">
            <span>入睡时间</span>
            <br />
            <span>未打卡</span>
          </div>
          <div class="nritsj12">
            <span>早起时间</span>
            <br />
            <span>未打卡</span>
          </div>
        </div>
      </div>
      <!-- 今日专注模块 -->
      <div class="nirw">
        <div class="nritwz">今日专注</div>
        <div class="nirw11">
          <span>专注时长</span>
          <br />
          <span>0分</span>
        </div>
        <div class="nirw11">
          <span>专注次数</span>
          <br />
          <span>0次</span>
        </div>
        <div class="nirw11">
          <span>放弃次数</span>
          <br />
          <span>0次</span>
        </div>
      </div>
      <!-- 今日冥想模块 -->
      <div class="nirw">
        <div class="nritwz">今日冥想</div>
        <div class="nirw11">
          <span>冥想时长</span>
          <br />
          <span>0分</span>
        </div>
        <div class="nirw11">
          <span>冥想次数</span>
          <br />
          <span>0次</span>
        </div>
        <div class="nirw11">
          <span>放弃次数</span>
          <br />
          <span>0次</span>
        </div>
      </div>
    </div>
    <div>
      <!-- 底部选项卡 -->
      <mt-tabbar v-model="selectedTab" fixed class="tab">
        <mt-tab-item id="home">
          <router-link to="/">首页</router-link>
          <img src="../assets/home_gray.png" slot="icon" v-if="selectedTab == 'home'" />
          <img src="../assets/home_red.png" slot="icon" v-else />
        </mt-tab-item>
        <mt-tab-item id="sound">
          <router-link to="sound">声音</router-link>
          <img src="../assets/sound_gray.png" slot="icon" v-if="selectedTab == 'sound'" />
          <img src="../assets/sound_red.png" slot="icon" v-else />
        </mt-tab-item>
        <mt-tab-item id="center">
          <router-link to="focus">专注</router-link>
          <img src="../assets/focus_gray.png" slot="icon" v-if="selectedTab == 'focus'" />
          <img src="../assets/focus_red.png" slot="icon" v-else />
        </mt-tab-item>
        <mt-tab-item>
          <router-link to="me">我的</router-link>
          <img src="../assets/me_gary.png" alt slot="icon" v-if="selecedTab == 'me'" />
          <img src="../assets/me_red.png" alt slot="icon" v-else />
        </mt-tab-item>
      </mt-tabbar>
      <!-- 底部选项卡结束 -->
    </div>
  </div>
</template>
<style scoped>
.loginw {
  width: 91%;
  background: #1ed;
  padding: 1rem;
  font-size: 18px;
  border-radius: 50px;
  margin: 1rem 0;
}
/* 头部样式 */
.top {
  background-color: #fff;
  width: 100%;
  position: fixed;
  margin-top: -5rem;
  /* background-color: rgb(255, 255, 255); */
}
/* 主要内容 */
.zynr {
  margin-top: 5rem;
  margin-bottom: 5rem;
}
/* 头部文字样式 */
.topw {
  width: 100%;
  /*height: 5rem;*/
  font-size: 26px;
  margin: 1rem;
  font-weight: bold;
}
/* 昨日睡眠样式 */
.nrit {
  border: 1px black solid;
  /*width: 22rem;*/
  margin-left: 1rem;
  margin-right: 1rem;
  height: 10rem;
}
/* 昨日睡眠文字的样式 */
.nritwz {
  border-bottom: 0.5px black solid;
  margin-top: 1rem;
  font-size: 1.5rem;
  margin-left: 1rem;
  margin-right: 1rem;
  padding-bottom: 0.5rem;
}
/* 昨日睡眠文字内部样式 */
.nritsj11 {
  float: left;
  margin: 3rem;
  font-size: 1rem;
  text-align: center;
}
.nritsj12 {
  float: left;
  margin: 3rem;
  font-size: 1rem;
  text-align: center;
}
.nirw11 {
  float: left;
  padding-top: 2rem;
  padding-left: 1rem;
  margin: 1rem;
  font-size: 1rem;
  text-align: center;
}
/* 今日专注和今日冥想样式 */
.nirw {
  border: 1px black solid;
  /*width: 22rem;*/
  margin: 0.5rem 1rem;
  height: 10rem;
}
.mint-navbar .mint-tab-item.is-selected {
  border-bottom: 3px solid white;
  color: #26a2ff;
  margin-bottom: -3px;
}
.mint-navbar {
  margin-bottom: 1rem;
}
</style>
<script>
export default {
  data() {
    return {
      n: "",
      active: 1,
    };
  },
};
</script>
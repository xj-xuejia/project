<template>
  <div>
    <!-- 头部 -->
    <div class="fhtb">
      <router-link to="/me">
        <img src="../assets/return.png" />
      </router-link>
    </div>
    <div class="top">
      <h1>登录之后更精彩</h1>
      <span>雨声睡眠期待与你相遇</span>
    </div>
    <!-- 登录框 -->
    <div class="denglu">
      <mt-field type="text" label="用户名" placeholder="请输入用户名"></mt-field>
      <mt-field type="password" label="密码" disableClear placeholder="请输入密码"></mt-field>
      <mt-field
        type="password"
        label="确认密码"
        placeholder="请再次输入密码"
        :attr="{maxlength:'10',autocomplete:'off'}"
      ></mt-field>
      <input type="button" value="提交" />
    </div>
    <!-- 底部图标 -->
    <div class="tubiao">
      <a href>
        <img src="../assets/wb.png" alt />
      </a>
      <a href>
        <img src="../assets/QQ.png" alt />
      </a>
      <div class="wzts">
        <h5>登录即代表您已经同意《用户协议》和《隐私协议》</h5>
      </div>
    </div>
  </div>
</template> 
<style scoped>
.top {
  margin-top: 3rem;
  margin-left: 3rem;
  margin-bottom: 3rem;
}
.top > h1 {
  font-weight: bolder;
  font-size: 2rem;
  padding-bottom: 1rem;
}
.denglu {
  margin-left: 5%;
  margin-right: 5%;
  border-bottom: 1px solid black;
}
.denglu > input {
  margin-left: 5rem;
  text-align: center;
  border-radius: 10px;
  padding: 0.3rem 2rem;
  margin-bottom: 0.7rem;
  background: #aaf;
  /*outline: none;*/
  border: 0;
}
.tubiao {
  margin-top: 5rem;
  /* text-align: center; */
  margin: 3rem;
}
.tubiao > a > img {
  width: 2rem;
  margin-left: 5rem;
}
.wzts {
  text-align: center;
  margin-top: 2rem;
}
</style>
<script>
</script> 
<template>
  <div id="app">
    <div id="nav">
      <!--
        
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link>
      
      <router-link to="/">主页</router-link>|
      <router-link to="/sound">声音</router-link>|
      <router-link to="/focus">专注</router-link>|
      <router-link to="/me">我的</router-link>
      <h1>這是主頁</h1>

      -->
      <router-view />
    </div>
  </div>
</template>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  /*text-align: center;*/
  color: #2c3e50;
}
/*#app div {
  background-color: #e1e1e2;
}


#nav {
  padding: 10px;
  background-color: #faafff;
}

#nav a.router-link-exact-active {
  color: #42b983;
}*/
#nav a {
  font-weight: bold;
  color: #000;
  text-decoration: none;
}
.mint-tabbar > .mint-tab-item.is-selected {
  /* background-color: #eaeaea; */
  color: #26a2ff;
}
</style>

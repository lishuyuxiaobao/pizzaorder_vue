<template>
  <div class="nav">
    <h3>
      <i class="fa fa-dribbble"></i>
      Pizza点餐系统
    </h3>
    <ul class="nav-action">
      <li>
        <router-link to="/">主页</router-link>
      </li>
      <li>
        <router-link to="/menu">菜单</router-link>
      </li>
      <li>
        <router-link to="/manage">管理</router-link>
      </li>
      <li>
        <router-link to="/about">关于我们</router-link>
      </li>
    </ul>
    <ul class="nav-lr">
      <li>
        <router-link to="/login">登录</router-link>
      </li>
      <li>
        <router-link to="/register">注册</router-link>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "Nav"
};
</script>

<style scoped>
.nav {
  padding: 1rem 0;
  background-color: rgb(252, 252, 249);
}
h3 {
  padding-left: 22px;
  position: relative;
  font-weight: 400;
  line-height: 1.2;
  cursor: pointer;
}
h3 i {
  width: 30px;
  height: 30px;
  position: absolute;
  left: 0;
  top: 2px;
  color: rgb(35, 35, 236);
  cursor: pointer;
}
h3 i:hover {
  color: rgb(11, 11, 88);
}
.nav {
  max-width: 1000px;
  display: flex;
  margin: 0 auto;
}
.nav-action {
  list-style-type: none;
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  grid-gap: 0.5rem;
  cursor: pointer;
}
.nav-action li a {
  text-decoration: none;
  outline: none;
  color: black;
  padding-left: 1rem;
}
.nav-lr {
  margin-left: 8rem;
  list-style-type: none;
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  grid-gap: 1rem;
  cursor: pointer;
}
.nav-lr li a {
  text-decoration: none;
  outline: none;
  color: black;
  padding-left: 1rem;
}
.nav .nav-action li a,
.nav .nav-lr li a {
  opacity: 0.6;
}
.nav .nav-action li a:hover,
.nav .nav-lr li a:hover {
  opacity: 1;
}
</style>

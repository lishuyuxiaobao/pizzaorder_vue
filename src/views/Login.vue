<template>
  <div class="login">
    <img src="../assets/login.png" />
    <div class="login-input">
      <label>邮箱</label>
      <input type="text" />
      <br />
      <label>密码</label>
      <input type="password" />
      <button @click="handleLogin">登录</button>
    </div>
  </div>
</template>

<script>
export default {
  name: "Login",
  data() {
    return {
      user: {
        email: "",
        password: ""
      }
    };
  },
  methods: {
    handleLogin() {
      this.$axios
        .get("https://wd4782151544jfcwop.wilddogio.com/lsyuser.json")
        .then(res => {
          this.user = res.data;
          console.log(JSON.stringify(res.data));
        })
        .catch(err => {
          console.log(err);
        });
    }
  }
};
</script>

<style scoped>
.login {
  max-width: 1000px;
  margin: 0 auto;
  padding: 1rem 1.5rem;
  margin-top: 0.5rem;
  border: 1px solid #cccccc;
  text-align: center;
  box-sizing: border-box;
}
.login-input label {
  text-align: left;
  display: block;
  color: #212529;
  font-size: 1.2rem;
}
.login-input input,
.login-input button {
  display: block;
  color: #212529;
  font-size: 1.2rem;
  width: 100%;
  box-sizing: border-box;
  padding: 0.4rem 0.6rem;
  outline: none;
  border: 1px solid #cccccc;
  border-radius: 0.5rem;
}
.login-input button {
  background: #28a745;
  color: #ffffff;
  margin-top: 1rem;
  cursor: pointer;
}
</style>
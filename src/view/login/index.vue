<template>
  <div id="login">
    <div class="login-box">
      <div class="title">vueSysTemplate</div>
      <div class="child-box"  v-if="!isRegister">
        <el-input placeholder="your username" v-model="user"> </el-input>
        <el-input placeholder="your password" show-password v-model="password"> </el-input>

        <el-button type="primary">login</el-button>
        <el-button @click="isRegister = !isRegister" type="primary"
          >register</el-button
        >
      </div>
      <div class="child-box" v-if="isRegister">
        <el-input placeholder="your username" v-model="user"> </el-input>
        <el-input placeholder="your password" show-password v-model="password"> </el-input>
        <el-button @click="isRegister = !isRegister" type="primary"
          >return</el-button
        >
        <el-button type="primary">comfirm</el-button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "login",
  data() {
    return {
      user: "",
      password: "",
      isRegister: false,
    };
  },
};
</script>

<style>
#login {
  background-color: #94faf534;
  height: 100vh;
  width: 100vw;
  text-align: center;
}
#login .login-box .title {
  font-size: 24px;
  color: #01201f;
  padding: 20px 0;
}
#login .login-box {
  height: 300px;
  width: 400px;
  background-color: #94faf5;
  margin: auto;
  border-radius: 20px;
  position: absolute;
  top: 0;
  bottom: 0;
  left: 0;
  right: 0;
  padding: 0 20px;
}
#login .login-box .child-box {
  width: 80%;
  margin: auto;
}
#login .login-box .child-box > .el-input {
  margin: 14px 0;
}
#login .login-box .child-box > .el-button {
  margin: 14px 0;
  width: 48%;
}
</style>

<template>
  <div class="login-container">
    <h2><img src="https://img.shields.io/badge/-freedom-646CFF?logo=vite&logoColor=white&style=for-the-badge" alt="logo"></h2>
    <input v-model="username" type="text" placeholder="用户名" />
    <input v-model="password" type="password" placeholder="密码" />
    <button @click="login">登录</button>
  </div>
</template>

<script setup lang="ts">
import { useRouter } from 'vue-router';

const router = useRouter();

const login = () => {
  // 使用 router.push 进行路由切换
  console.log('router', router)
  router.push('/home');
};
</script>

<style scoped>
.login-container {
  background-color: #ffffff;
  border-radius: 8px;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
  padding: 20px;
  width: 300px;
  text-align: center;
}

.login-container input {
  width: 80%;
  padding: 10px;
  margin-bottom: 15px;
  border: 1px solid #ccc;
  border-radius: 4px;
}

.login-container button {
  width: 80%;
  padding: 10px;
  background-color: #007bff;
  color: #fff;
  border: none;
  border-radius: 4px;
  cursor: pointer;
}

.login-container button:hover {
  background-color: #0056b3;
}
</style>

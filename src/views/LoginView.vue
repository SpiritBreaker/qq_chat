<template>
  <div class="about">
    <h1>Login page here</h1>
    <el-button type="primary" @click="onLogin">Login</el-button>
  </div>
</template>

<script setup>
import { useRoute, useRouter } from 'vue-router'

const router = useRouter()
const onLogin = async () => {
  router.push('/home')
}
</script>

<style scoped lang="scss">

</style>

<script setup>
import { ref } from 'vue'
import Sidebar from '../components/Sidebar.vue'
import HomeBody from '../components/HomeBody.vue'
</script>

<template>  <div class="layout__wrapper">
    <el-row style="height: 100vh;">
        <Sidebar/>
        <HomeBody/>
    </el-row>
  </div>
</template>

<style scoped>
.layout__wrapper {
  width: 100vw;
  height: 100vh;
}
</style>
<script setup>
import { ref } from 'vue'
import { useRouter } from 'vue-router'
const status = ref(false)
const router = useRouter()

function handleLogin () {
    status.value = true
    setTimeout(function () {
        status.value = false
        router.push('/home')
    }, 2000)
}
</script>

<template>
    <el-button type="primary" :loading="status" @click="handleLogin">Login with Google {{ count }}</el-button>
</template>
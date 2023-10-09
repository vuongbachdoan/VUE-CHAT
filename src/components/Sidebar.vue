<script setup>
import { ChatLineRound, Phone, Setting, Cellphone } from '@element-plus/icons-vue'
</script>

<template>
    <el-col class="flex flex-col items-center p-3 gap-3" :span="1">
        <el-button style="margin: 0" :icon="ChatLineRound" circle />
        <el-button style="margin: 0" :icon="Phone" circle />
        <div class="flex-1"></div>
        <el-button style="margin: 0" :icon="Setting" circle />
        <el-button style="margin: 0" :icon="Cellphone" circle />
    </el-col>
</template>
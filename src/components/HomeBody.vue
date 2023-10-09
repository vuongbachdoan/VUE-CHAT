<script setup>
import { ref } from 'vue'
import { Search } from '@element-plus/icons-vue'
const input1 = ref('')
</script>

<template>
    <el-col :span="23" class="pt-3 pe-3 h-full">
        <el-container class="bg-slate-300 rounded-t-lg h-full row">
            <el-col :span="6" class="bg-slate-600 rounded-tl-lg p-3">
                <el-input v-model="input1" class="w-full rounded-lg" size="large" placeholder="Search"
                    :suffix-icon="Search" />
                <el-card class="mt-3 rounded-lg">
                    <div class="item flex flex-row gap-3">
                        <el-avatar :size="50"
                            src="https://cube.elemecdn.com/3/7c/3ea6beec64369c2642b92c6726f1epng.png" />
                        <div>
                            <p class="font-semibold">Bach Doan Vuong</p>
                            <p>Hello.</p>
                        </div>
                    </div>
                </el-card>
            </el-col>
            <el-col :span="18" class="flex flex-col">
                <el-container class="flex-1"></el-container>
                <div style="height: 200px;" class="w-full p-3">
                    <el-card class="w-full rounded-lg h-full">
                    </el-card>
                </div>
            </el-col>
        </el-container>
    </el-col>
</template>
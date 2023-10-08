<template>
  <div>
    <el-row>
      <el-col :span="18">
        <!-- <el-dialog title="Chat Room" :visible.sync="data.dialogVisible" width="50%"> -->
        <el-dialog v-model="data.dialogVisible" title="Chat Room" width="50%">
          <div v-for="message in data.messages">
            <el-avatar :src="message.avatar"/>
            <span>{{ message.name }}:</span>
            <span>{{ message.content }}</span>
          </div>
          <el-input v-model="data.input" placeholder="Type your message here"></el-input>
          <el-button type="primary" @click="sendMessage">Send</el-button>
        </el-dialog>
      </el-col>

      <el-col :span="6">
        <el-badge :value="data.unreadCount">
          <el-button type="text" @click="showDialog">Open Chat</el-button>
        </el-badge>
      </el-col>
    </el-row>
  </div>
</template>

<script setup>
import { ref } from 'vue'
const data = ref(
  {
    dialogVisible: false,
    input: '',
    messages: [
      { name: 'John', avatar: 'https://randomuser.me/api/portraits/men/1.jpg', content: 'Hello' },
      { name: 'Jane', avatar: 'https://randomuser.me/api/portraits/women/1.jpg', content: 'Hi' }
    ],
    unreadCount: 0
  }
)

function showDialog() {
  data.value.dialogVisible = true
}

function sendMessage() {
  if (data.value.input) {
    data.value.messages.push({ name: 'You', avatar: 'https://randomuser.me/api/portraits/men/2.jpg', content: data.value.input })
    data.value.input = ''
    data.value.unreadCount++
  }
}
</script>

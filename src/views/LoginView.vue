<template>
  <div class="login-container">
    <div class="align-center">
      <img class="img-logo" src="../assets/image/logo.png" />
    </div>
    <p class="align-center login-title">로그인</p>
    <div class="login-inputs">
      <span>아이디</span>
      <input type="text" v-model="id" />
    </div>

    <div class="login-inputs">
      <span>비밀번호</span>
      <input type="password" v-model="pw" />
    </div>

    <div class="align-center">
      <button
        class="btn"
        :class="{ disabled: !buttonActive }"
        @click="doLogin()"
        :disabled="!buttonActive"
      >
        로그인
      </button>
    </div>

    <p class="align-center login-ver">ver 1.0</p>
  </div>
</template>

<script setup lang="ts">
import { ref, watch } from 'vue'

const id = ref<string>('')
const pw = ref<string>('')
const buttonActive = ref<boolean>(false)

watch([id, pw], ([nId, nPw]) => {
  if (nId && nPw) {
    buttonActive.value = true
  }
})
</script>

<script lang="ts">
export default {
  methods: {
    doLogin() {
      this.$router.push('/')
    }
  }
}
</script>

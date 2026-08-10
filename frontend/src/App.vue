<script setup>
import { ref } from 'vue'
import CreateAccountPage from './views/CreateAccountPage.vue'
import LoginPage from './views/LoginPage.vue'

const currentView = ref('create')

function switchToLogin() {
  currentView.value = 'login'
}

function switchToCreate() {
  currentView.value = 'create'
}
</script>

<template>
  <CreateAccountPage v-if="currentView === 'create'" @go-to-login="switchToLogin" />
  <LoginPage v-else @go-to-create="switchToCreate" />
</template>

<template>
  <div class="grid grid-cols-2 h-screen">
    <div class="bg-secondary-color"></div>

    <div class="flex justify-center items-center h-full">
      <LoginForm />
    </div>
  </div>
</template>

<script setup lang="ts">
import LoginForm from "@/components/views/login/LoginForm.vue";
</script>

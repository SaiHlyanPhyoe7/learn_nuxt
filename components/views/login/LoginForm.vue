<template>
  <div class="w-full md:max-w-[26rem] p-6 space-y-4">
    <h4 class="text-black text-2xl pb-3">
      Welcome to <span class="text-primary-color font-semibold">Toon CMS</span>
    </h4>
    <div class="space-y-6">
      <Input type="text" placeholder="Enter your email" label="Email" />
      <Input type="password" placeholder="Enter your password" label="Password" />

      <div class="flex justify-between items-center">
        <p class="text-xs text-primary-color hover:underline cursor-pointer">
          Forgot Password?
        </p>
        <Button class="ml-auto w-40" @click="login">Login</Button>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
import { ref } from 'vue';
import Input from "@/components/ui/form/Input.vue";
import Button from "@/components/ui/form/Button.vue";

const email = ref("");
const password = ref("");

const login = () => {
  console.log(email.value, password.value);
};
</script>

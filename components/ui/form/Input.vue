<template>
  <div class="w-full relative">
    <label v-if="label" class="block text-xs font-medium text-gray-700 mb-1.5">{{ label }}</label>
    <input
      :type="isPassword ? (showPassword ? 'text' : 'password') : type"
      :placeholder="placeholder"
      class="w-full px-2 py-3 rounded-sm text-sm border focus:border-primary-color focus:shadow-outline focus:outline-primary-color active:border-primary-color"
      {...props}
    />
    <div v-if="isPassword"  class="absolute inset-y-0 right-0 top-6 pr-3 flex items-center text-xs leading-5 cursor-pointer">
      <span class="bg-transparent border shadow-sm hover:opacity-100 opacity-80 border-primary-color text-primary-color w-16 h-8 flex justify-center items-center rounded-sm" @click="togglePassword">
      {{ showPassword ? 'Hide' : 'Show' }}
    </span>
    </div>
  </div>
</template>

<script setup lang="ts">
import { ref, defineProps } from 'vue';

const props = defineProps({
  label: {
    type: String,
    default: ''
  },
  placeholder: {
    type: String,
    default: ''
  },
  type: {
    type: String,
    default: 'text'
  }
});

const showPassword = ref(false);

const isPassword = props.type === 'password';

const togglePassword = () => {
  showPassword.value = !showPassword.value;
};
</script>


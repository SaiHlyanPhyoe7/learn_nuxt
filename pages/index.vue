<template>
  <div>
    Test 16
  </div>
  <a-button @click="handleMessage">
    button
  </a-button>
</template>

<script setup lang="ts">
const handleMessage = () => {
  message.info("This is a normal message");
}
</script>

<style lang="scss" scoped>

</style>
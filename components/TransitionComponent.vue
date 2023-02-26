<script setup lang="ts">
import { ref } from 'vue'
const show = ref(false);

const onClick = () => {
  show.value = !show.value
}
</script>
<style>
.v-enter-active,
.v-leave-active {
  transition: opacity 0.5s ease;
}

.v-enter-from,
.v-leave-to {
  opacity: 0;
}
</style>

<template>
  <button @click="onClick">Show Text</button>
  <Transition>
    <p v-if="show">Hello guys!</p>
  </Transition>
</template>

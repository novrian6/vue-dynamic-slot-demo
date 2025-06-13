<template>
  <div class="mb-4">
    <button @click="currentComponent = 'HelloWorld'" class="btn">Show Hello</button>
    <button @click="currentComponent = 'GoodbyeWorld'" class="btn ml-2">Show Goodbye</button>

    <!-- Render the actual component instance -->
    <component :is="components[currentComponent]" />
  </div>
</template>

<script setup>
import { ref } from 'vue'
import HelloWorld from './HelloWorld.vue'
import GoodbyeWorld from './GoodbyeWorld.vue'

const currentComponent = ref('HelloWorld')

// Map string to component object
const components = {
  HelloWorld,
  GoodbyeWorld
}

defineExpose({
  currentComponent
})
</script>

<style scoped>
.btn {
  background-color: #3b82f6;
  color: white;
  padding: 8px 12px;
  border: none;
  border-radius: 6px;
  cursor: pointer;
}
</style>
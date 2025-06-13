<template>
  <div class="max-w-xl mx-auto mt-10 space-y-6">
    <h1 class="text-2xl font-bold text-center">Vue 3 Dynamic Component and Slot Demo</h1>

    <!-- Dynamic Component Section -->
    <DynamicComponentWrapper />
    <hr>

    <!-- Slot Usage Section -->
    <SlotExample>
      <p>This is injected into the default slot...</p>

      <template #footer>
        <p class="text-sm text-gray-500">This is injected into the footer slot.</p>
      </template>
    </SlotExample>
  </div>
</template>

<script setup>
import DynamicComponentWrapper from './components/DynamicComponentWrapper.vue'
import SlotExample from './components/SlotExample.vue'
</script>
<template>
  <div class="p-4 border rounded bg-gray-50">
    <h2 class="font-bold mb-2">This is the Slot Wrapper</h2>

    <!-- Default slot -->
    <slot>This is fallback content</slot>

    <!-- Named slot -->
    <div class="mt-4">
      <slot name="footer" />
    </div>
  </div>
</template>

<script setup>
</script>
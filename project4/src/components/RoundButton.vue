<template>
  <button
    class="text-sm font-medium border border-gray-200 rounded-full px-3 py1 hover:bg-gray-200"
    @click="$emit('click')"
  >
    <slot></slot>
  </button>
</template>

<script setup>
defineEmits(["click"])
</script>
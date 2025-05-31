<template>
  <div class="border border-gray-200 bg-white rounded-md">
    <h3 class="p-4 font-medium text-xl border-b border-gray-200">{{ title }}</h3>
    <p class="p-4 border-b border-gray-200">
      {{ when.toLocaleString('zh-TW', { year: 'numeric', month: '2-digit', day: '2-digit', hour: '2-digit', minute: '2-digit' }) }}
    </p>
    <p class="p-4">{{ description }}</p>
    <section class="flex justify-end p-4">
      <RoundButton label="register" @click="$emit('register')">
        Register
      </RoundButton>
    </section>
  </div>
</template>

<script setup>
import RoundButton from "@/components/RoundButton.vue";

defineProps({
  title: String,
  when: Date,
  description: String
});
defineEmits(["register"]);
</script>
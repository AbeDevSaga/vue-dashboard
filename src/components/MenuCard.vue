<template>
  <div class="flex items-center justify-between px-[10px] h-[40px]">
    <div class="flex items-center">
      <span class="font-semibold">{{ text }}</span>
    </div>
  </div>
</template>

<script lang="ts" setup>
import { defineProps } from "vue";

const { text } = defineProps<{ text: string }>();
</script>

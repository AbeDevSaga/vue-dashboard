<template>
  <a
    :href="link"
    class="flex items-center w-[200px] h-[48px] p-2 rounded hover:bg-gray-100 transition"
  >
    <!-- Left Icon -->
    <span
      class="flex-shrink-0"
      :style="{
        width: `${iconSize}px`,
        height: `${iconSize}px`,
        color: 'var(--color-primary)',
      }"
    >
      <component :is="icon" />
    </span>

    <!-- Text -->
    <span class="ml-3" :style="{ color: 'var(--color-text)' }">
      {{ text }}
    </span>
  </a>
</template>

<script lang="ts" setup>
import { defineProps } from "vue";

const props = defineProps<{
  text: string;
  link?: string;
  icon: any; // pass Vue component
  iconSize?: number;
}>();

const iconSize = props.iconSize ?? 18;
const link = props.link ?? "#";
</script>

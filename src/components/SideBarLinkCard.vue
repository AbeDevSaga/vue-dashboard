<template>
  <a
    :href="link"
    class="flex items-center w-full h-[48px] px-[12px] space-x-[13px]"
  >
    <!-- Left Icon -->
    <div
      class="w-[24px] h-[24px] flex primary-text items-center justify-center"
    >
      <img :src="iconSrc" :alt="iconAlt" class="w-[18px] h-[18px]" />
    </div>

    <!-- Text -->
    <span class="title">
      {{ text }}
    </span>
  </a>
</template>

<script lang="ts" setup>
import { defineProps } from "vue";

const props = defineProps<{
  text: string;
  link?: string;
  iconSrc: string;
  iconAlt?: string;
}>();

const iconAlt = props.iconAlt ?? "icon";
</script>

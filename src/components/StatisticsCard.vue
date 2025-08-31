<template>
  <div
    class="flex items-center w-[314] px-[20px] h-[130px] space-x-[14px] border rounded-[6px]"
  >
    <!-- Left section: headline + footer -->
    <div
      class="flex primary items-center w-[65px] h-[65px] rounded-[10px] justify-center"
    >
      <div class="flex items-center w-[28px] h-[28px] justify-center">
        <img :src="iconSrc" :alt="iconAlt" class="w-[23px] h-auto" />
      </div>
    </div>

    <!-- Right section: dynamic image -->
    <div class="flex flex-col items-left">
      <span class="headline truncate">{{ headline }}</span>
      <span class="footer truncate">{{ footer }}</span>
    </div>
  </div>
</template>

<script lang="ts" setup>
import { defineProps } from "vue";

const props = defineProps<{
  headline: string;
  footer: string;
  iconSrc: string;
  iconAlt?: string;
}>();

const iconAlt = props.iconAlt ?? "icon";
</script>

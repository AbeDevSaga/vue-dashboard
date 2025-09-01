<template>
  <div
    class="flex items-center w-full px-[20px] h-[130px] space-x-[14px] border rounded-[10px]"
  >
    <!-- Left section: icon -->
    <div
      class="flex primary items-center p-[19px] h-[65px] rounded-[10px] justify-center"
    >
      <div class="flex items-center w-[28px] h-[28px] justify-center">
        <img :src="iconSrc" :alt="iconAlt" class="w-[23px] h-auto" />
      </div>
    </div>

    <!-- Right section: texts -->
    <div class="flex flex-col items-left truncate">
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

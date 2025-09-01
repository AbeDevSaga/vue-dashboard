<template>
  <div
    class="flex items-center justify-between w-[200px]"
  >
    <!-- Left section: avatar + user info -->
    <div class="flex items-center gap-2">
      <!-- Circle avatar -->
      <div
        class="flex items-center justify-center rounded-full text-white font-semibold"
        :style="{
          width: `${avatarSize}px`,
          height: `${avatarSize}px`,
          backgroundColor: 'var(--color-primary)',
        }"
      >
        {{ name.charAt(0).toUpperCase() }}
      </div>

      <!-- User info -->
      <div class="flex flex-col user max-w-[100px]">
        <span class="text-[14px]  truncate">{{ name }}</span>
        <span class="text-[12px] truncate">{{ email }}</span>
      </div>
    </div>

    <!-- Right section: open/collapse icon stacked vertically -->
    <div class="flex items-center w-[20px] h-[20px]">
      <img src="../assets/Vector.svg" alt="icon" class="w-[12px] h-auto" />
    </div>
  </div>
</template>

<script lang="ts" setup>
import { defineProps } from "vue";

const props = defineProps<{
  name: string;
  email: string;
  avatarSize?: number;
}>();

const avatarSize = props.avatarSize ?? 40;
</script>

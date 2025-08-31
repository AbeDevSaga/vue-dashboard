<template>
  <div
    class="flex items-center justify-between h-[40px] px-[16px] border rounded-[6px]"
  >
    <CalenderCard />
    <MenuCard text="1d" />
    <MenuCard text="3d" />
    <MenuCard text="7d" />
    <MenuCard text="30d" />
    <MenuCard text="All" />
  </div>
</template>

<script lang="ts" setup>
import MenuCard from "./MenuCard.vue";
import CalenderCard from "./CalenderCard.vue";
</script>

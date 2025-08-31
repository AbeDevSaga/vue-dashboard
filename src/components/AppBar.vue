<template>
  <header
    class="w-full pt-[20px] px-[20px] flex items-center justify-end"
  >
    <div class="flex items-center space-x-[20px]">
      <SourceFilterCard />
      <FilterMenuCard />
      <FilterButton />
      <DownloadButton />
    </div>
  </header>
</template>

<script lang="ts" setup>
import SourceFilterCard from "./SourceFilterCard.vue";
import FilterMenuCard from "./FilterMenuCard.vue";
import FilterButton from "./FilterButton.vue";
import DownloadButton from "./DownloadButton.vue";
</script>

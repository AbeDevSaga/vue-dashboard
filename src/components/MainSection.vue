<template>
  <main class="flex-1 flex-col p-[24px] space-y-[24px] overflow-y-auto hide-scrollbar">
    <div class="w-full grid md:grid-cols-2 lg:grid-cols-3 gap-[24px]">
      <StatisticsCard
        headline="Total waiting list"
        footer="43"
        :iconSrc="listIcon"
        iconAlt="list"
      />
      <StatisticsCard
        headline="New signups today"
        footer="5"
        :iconSrc="plusIcon"
        iconAlt="new"
      />
      <StatisticsCard
        headline="Top source"
        footer="LinkedIn"
        :iconSrc="linkedInIcon"
        iconAlt="LinkedIn"
      />
    </div>
    <WaitingListCard />
    <ChartSection />
  </main>
</template>

<script lang="ts" setup>
import StatisticsCard from "./StatisticsCard.vue";
import WaitingListCard from "./WaitingListCard.vue";
import ChartSection from "./ChartSection.vue";
import listIcon from "../assets/list.svg";
import plusIcon from "../assets/plus.svg";
import linkedInIcon from "../assets/linked.svg";
</script>

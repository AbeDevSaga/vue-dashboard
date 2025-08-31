<template>
  <aside
    class="w-[240px] h-screen bg-background border shadow-md p-[20px] flex flex-col"
  >
    <!-- Logo Section -->
    <div class="w-[150px] mb-8">
      <img src="../assets/logo_teal.svg" alt="Logo" class="w-full h-auto" />
    </div>

    <nav class="flex flex-col gap-2">
      <SidebarLinkCard text="General" link="/" :icon="DashboardIcon" />
      <SidebarLinkCard
        text="Statistics"
        link="/statistics"
        :icon="StatisticsIcon"
      />
      <SidebarLinkCard
        text="Waiting List"
        link="/waiting-list"
        :icon="WaitingListIcon"
      />
      <SidebarLinkCard text="Admins" link="/admins" :icon="AdminsIcon" />
      <SidebarLinkCard
        text="Profile Settings"
        link="/profile"
        :icon="ProfileIcon"
      />
    </nav>

    <!-- User Profile Card at the bottom -->
    <div class="mt-auto pt-6">
      <UserProfileCard
        name="Aman Dan"
        email="aman@example.com"
        :collapseIcon="CollapseIcon"
        :openIcon="OpenIcon"
      />
    </div>
  </aside>
</template>

<script lang="ts" setup>
import SidebarLinkCard from "./SideBarLinkCard.vue";
import UserProfileCard from "./UserProfileCard.vue";

// SVG icons
import DashboardIcon from "./icons/DashboardIcon.vue";
import StatisticsIcon from "./icons/StatisticsIcon.vue";
import WaitingListIcon from "./icons/WaitingListIcon.vue";
import AdminsIcon from "./icons/AdminsIcon.vue";
import ProfileIcon from "./icons/ProfileIcon.vue";
import CollapseIcon from "./icons/CollapseIcon.vue";
import OpenIcon from "./icons/OpenIcon.vue";
</script>

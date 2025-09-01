<template>
  <aside
    class="w-[240px] h-screen bg-background border shadow-md p-[20px] flex flex-col"
  >
    <!-- Logo Section -->
    <div class="w-[150px] mb-8">
      <img src="../assets/logo_teal.svg" alt="Logo" class="w-full h-auto" />
    </div>

    <nav class="flex flex-col gap-2">
      <SidebarLinkCard
        text="General"
        link="/"
        :icon="dashboardIcon"
        iconAlt="Dashboard"
      />
      <SidebarLinkCard
        text="Statistics"
        link="/statistics"
        :iconSrc="statIcon"
        iconAlt="Statistics"
      />
      <SidebarLinkCard
        text="Waiting List"
        link="/waiting-list"
        :iconSrc="listIcon"
        iconAlt="Waiting List"
      />
      <SidebarLinkCard
        text="Admins"
        link="/admins"
        :icon="adminIcon"
        iconAlt="Admins"
      />
      <SidebarLinkCard
        text="Profile Settings"
        link="/profile"
        :iconSrc="profileIcon"
        iconAlt="Profile"
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
import adminIcon from "../assets/admin.svg";
import dashboardIcon from "../assets/dashboard.svg";
import profileIcon from "../assets/profile.svg";
import listIcon from "../assets/list.svg";
import statIcon from "../assets/stat.svg";

import ProfileIcon from "./icons/ProfileIcon.vue";
import CollapseIcon from "./icons/CollapseIcon.vue";
import OpenIcon from "./icons/OpenIcon.vue";
</script>

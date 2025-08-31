<template>
  <div class="flex h-screen">
    <!-- Sidebar -->
    <Sidebar />

    <!-- Main Area -->
    <div class="flex-1 flex flex-col">
      <AppBar />
      <MainSection />
    </div>
  </div>
</template>

<script lang="ts" setup>
import Sidebar from './components/Sidebar.vue'
import AppBar from './components/AppBar.vue'
import MainSection from './components/MainSection.vue'
</script>

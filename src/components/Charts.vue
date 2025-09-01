<script setup lang="ts">
import {
  Chart as ChartJS,
  Title,
  Tooltip,
  Legend,
  ArcElement,
  BarElement,
  LineElement,
  PointElement,
  CategoryScale,
  LinearScale,
} from "chart.js";
import { Pie, Bar, Line } from "vue-chartjs";

// Register chart.js components
ChartJS.register(
  Title,
  Tooltip,
  Legend,
  ArcElement,
  BarElement,
  LineElement,
  PointElement,
  CategoryScale,
  LinearScale
);

// Pie chart data
const pieData = {
  labels: ["Google", "Facebook", "Twitter", "Direct"],
  datasets: [
    {
      label: "Signups",
      data: [40, 25, 20, 15],
      backgroundColor: ["#3b82f6", "#22c55e", "#f59e0b", "#ef4444"],
    },
  ],
};

// Bar chart data
const barData = {
  labels: ["Jan", "Feb", "Mar", "Apr"],
  datasets: [
    {
      label: "Signups",
      data: [65, 59, 80, 81],
      backgroundColor: "#3b82f6",
    },
  ],
};

// Line chart data (waiting list trend)
const lineData = {
  labels: ["Week 1", "Week 2", "Week 3", "Week 4"],
  datasets: [
    {
      label: "Waiting List Entries",
      data: [12, 19, 14, 22],
      borderColor: "#10b981",
      backgroundColor: "rgba(16,185,129,0.3)",
      tension: 0.4, // smooth curve
      fill: true,
    },
  ],
};

const options = {
  responsive: true,
  maintainAspectRatio: false,
};
</script>

<template>
  <!-- Full-width Line Chart -->
  <div class="w-full h-[269px] flex items-center justify-center border rounded-[10px]">
    <Line :data="lineData" :options="options" />
  </div>

  <!-- Grid with Pie and Bar -->
  <div class="w-full h-[241px] grid grid-cols-3 gap-[24px]">
    <!-- Pie Chart -->
    <div
      class="w-full max-h-[241px] flex items-center justify-center border rounded-[10px] p-[10px]"
    >
      <Pie :data="pieData" :options="options" />
    </div>

    <!-- Bar Chart -->
    <div
      class="w-full max-h-[241px] col-span-2 flex items-center justify-center border rounded-[10px] p-[10px]"
    >
      <Bar :data="barData" :options="options" />
    </div>
  </div>
</template>

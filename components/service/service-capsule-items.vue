<template>
  <div class="tp-services-capsule-item-wrapper">
    <p v-for="(s, i) in services" :key="i" data-tp-throwable-el="">
      <span
        class="tp-services-capsule-item"
        :data-bg-color="s.bgColor"
        :data-text-color="`${s.textColor ? s.textColor : ''}`"
        :style="{ backgroundColor: s.bgColor, color: s.textColor }"
      >
        {{ s.name }}
      </span>
    </p>
    <p data-tp-throwable-el="">
      <span>
        <img src="/images/services/shape/services-shape-1.png" alt="" />
      </span>
    </p>
    <p data-tp-throwable-el="">
      <span>
        <img src="/images/services/shape/services-shape-2.png" alt="" />
      </span>
    </p>
  </div>
</template>

<script setup lang="ts">
const services = [
  { name: "Frontend Development", bgColor: "#00CC97" },
  { name: "React Development", bgColor: "#FF759C" },
  { name: "Next.js Applications", bgColor: "#FFDB59", textColor: "#121212" },
  { name: "Responsive Design", bgColor: "#FFDB59", textColor: "#121212" },
  { name: "UI Implementation", bgColor: "#00CC97" },
  { name: "Performance Optimization", bgColor: "#19B3F1" },
  { name: "Bug Fixing & Testing", bgColor: "#FF759C" },
  { name: "Problem Solving", bgColor: "#FFDB59", textColor: "#121212" },
  {
    name: "Cross-Browser Compatibility",
    bgColor: "#FFDB52",
    textColor: "#121212",
  },
  { name: "Vue.js Development", bgColor: "#FFDB45", textColor: "#121212" },
  { name: "WordPress (Elementor)", bgColor: "#FFDB22", textColor: "#121212" },
];
</script>

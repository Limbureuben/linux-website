<template>
  <div>
    <NuxtRouteAnnouncer />
    <Landing />
  </div>
</template>

<script setup>
import Landing from './landing.vue'
</script>

<style>
body, html {
  margin: 0;
  padding: 0;
  width: 100%;
  overflow-x: hidden;
}

/* Global Animation Utilities */
.animate-fade-up {
  opacity: 0;
  transform: translateY(20px);
  transition: opacity 0.8s cubic-bezier(0.16, 1, 0.3, 1), transform 0.8s cubic-bezier(0.16, 1, 0.3, 1);
  will-change: opacity, transform;
}

.animate-fade-up.active {
  opacity: 1;
  transform: translateY(0);
}

.animate-scale-in {
  opacity: 0;
  transform: scale(0.95);
  transition: opacity 0.8s cubic-bezier(0.16, 1, 0.3, 1), transform 0.8s cubic-bezier(0.16, 1, 0.3, 1);
  will-change: opacity, transform;
}

.animate-scale-in.active {
  opacity: 1;
  transform: scale(1);
}

.animate-slide-left {
  opacity: 0;
  transform: translateX(-50px);
  transition: opacity 0.8s cubic-bezier(0.16, 1, 0.3, 1), transform 0.8s cubic-bezier(0.16, 1, 0.3, 1);
  will-change: opacity, transform;
}

.animate-slide-left.active {
  opacity: 1;
  transform: translateX(0);
}

.animate-slide-right {
  opacity: 0;
  transform: translateX(50px);
  transition: opacity 0.8s cubic-bezier(0.16, 1, 0.3, 1), transform 0.8s cubic-bezier(0.16, 1, 0.3, 1);
  will-change: opacity, transform;
}

.animate-slide-right.active {
  opacity: 1;
  transform: translateX(0);
}

/* Hover Effects */
.hover-lift {
  transition: transform 0.3s cubic-bezier(0.34, 1.56, 0.64, 1), box-shadow 0.3s ease;
}

.hover-lift:hover {
  transform: translateY(-8px);
  box-shadow: 0 12px 30px rgba(0, 0, 0, 0.1);
}

.hover-glow {
  transition: all 0.3s ease;
}

.hover-glow:hover {
  box-shadow: 0 0 15px rgba(0, 71, 153, 0.3);
  filter: brightness(1.1);
}

/* Accessibility: Reduced Motion */
@media (prefers-reduced-motion: reduce) {
  .animate-fade-up,
  .animate-scale-in,
  .hover-lift {
    transition: none !important;
    opacity: 1 !important;
    transform: none !important;
  }
}
</style>

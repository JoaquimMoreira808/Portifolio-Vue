<script setup>
import FooterComponent from './components/FooterComponent.vue'
</script>

<template>
  <div class="min-h-screen flex flex-col bg-gradient-to-r from-black to-[#20233d]">
    <div class="container mx-auto px-4 py-6 flex-grow">
      <router-view />
    </div>
    <FooterComponent />
  </div>
</template>
<template>
  <button
    @click="goBack"
    class="bg-black text-white px-4 py-2 rounded-full text-5xl hover:opacity-50 transition"
  >
    ←
  </button>
</template>

<script setup>
import { useRouter } from 'vue-router'

const router = useRouter()

function goBack() {
  router.back()
}
</script>

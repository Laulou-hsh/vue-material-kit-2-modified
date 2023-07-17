<template>
  <div v-show="isShow" @click="scrollToTop" class="top-button">
    <slot></slot>
  </div>
</template>

<script setup>
import {ref, onMounted, onUnmounted} from 'vue'

const isShow = ref(false)
const scrollThreshold = 300

const handleScroll = () => {
  isShow.value = window.scrollY > scrollThreshold
}

const scrollToTop = () => {
  window.scrollTo({
    top: 0,
    behavior: 'smooth',
  })
}

onMounted(() => {
  window.addEventListener('scroll', handleScroll)
})

onUnmounted(() => {
  window.removeEventListener('scroll', handleScroll)
})
</script>

<style>
.top-button {
  position: fixed;
  bottom: 20px;
  right: 20px;
  background-color: #ccc;
  padding: 10px;
  cursor: pointer;
}
</style>

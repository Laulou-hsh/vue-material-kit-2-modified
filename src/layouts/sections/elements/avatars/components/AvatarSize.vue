<script setup>
//Vue Material Kit 2 components
import MaterialAvatar from '@/components/MaterialAvatar.vue'

// image
import Laulou from '@/assets/img/laulou.png'
</script>
<template>
  <div class="container py-6">
    <div class="row mt-5 text-center">
      <div class="col-12">
        <a href="javascript:;">
          <MaterialAvatar :image="Laulou" alt="Image placeholder" size="xs" />
        </a>
        <a href="javascript:;">
          <MaterialAvatar :image="Laulou" alt="Image placeholder" size="sm" />
        </a>
        <a href="javascript:;">
          <MaterialAvatar :image="Laulou" alt="Image placeholder" size="md" />
        </a>
        <a href="javascript:;">
          <MaterialAvatar :image="Laulou" alt="Image placeholder" size="lg" />
        </a>
        <a href="javascript:;">
          <MaterialAvatar :image="Laulou" alt="Image placeholder" size="xl" />
        </a>
        <a href="javascript:;">
          <MaterialAvatar :image="Laulou" alt="Image placeholder" size="xxl" />
        </a>
      </div>
    </div>
  </div>
</template>

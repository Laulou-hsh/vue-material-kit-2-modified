<script setup>
import {onMounted} from 'vue'

//Vue Material Kit 2 components
import MaterialAvatar from '@/components/MaterialAvatar.vue'

// images
import {data} from './AvatatData.json'
const AvatarData = data

// popover
import setTooltip from '@/assets/js/tooltip'

// store
import {useAppStore} from '@/stores'
const store = useAppStore()

// hook
onMounted(() => {
  setTooltip(store.bootstrap)
})
</script>
<template>
  <div class="container py-6">
    <div class="row mt-5 text-center">
      <div class="col-12">
        <div class="avatar-group">
          <a
            href="javascript:;"
            class="avatar avatar-lg"
            data-bs-toggle="tooltip"
            data-bs-placement="bottom"
            :title="item.title"
            :key="item.title"
            v-for="item in AvatarData"
          >
            <MaterialAvatar :image="item.image" alt="Image placeholder" size="lg" />
          </a>
        </div>
      </div>
    </div>
  </div>
</template>

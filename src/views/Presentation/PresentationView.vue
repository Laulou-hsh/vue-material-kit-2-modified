<script setup>
import {onMounted, onUnmounted} from 'vue'

//example components
import NavbarDefault from '../..//examples/navbars/NavbarDefault.vue'
import DefaultFooter from '../../examples/footers/FooterDefault.vue'
import Header from '../../examples/Header.vue'
import BackToTopButton from '../../examples/BackToTopButton.vue'

// sections
import PresentationCounter from './Sections/PresentationCounter.vue'
import PresentationExample from './Sections/PresentationExample.vue'
import data from './Sections/Data/designBlocksData'

//images
import vueMkHeader from '@/assets/img/vue-mk-header.jpg'

//hooks
const body = document.getElementsByTagName('body')[0]
onMounted(() => {
  body.classList.add('presentation-page')
  body.classList.add('bg-gray-200')
})
onUnmounted(() => {
  body.classList.remove('presentation-page')
  body.classList.remove('bg-gray-200')
})
</script>

<template>
  <div class="position-sticky z-index-sticky top-0">
    <div class="row">
      <div class="col-12">
        <NavbarDefault :sticky="true" />
      </div>
    </div>
  </div>
  <Header>
    <div class="page-header min-vh-75" :style="`background-image: url(${vueMkHeader})`" loading="lazy">
      <div class="container">
        <div class="row">
          <div class="col-lg-7 text-center mx-auto position-relative">
            <h1 class="text-white pt-3 mt-n5 me-2" :style="{display: 'inline-block '}">Material Kit 2</h1>
            <p class="lead text-white px-5 mt-3" :style="{fontWeight: '500'}">
              Start the Development With Bootstrap 5 Design System inspired by Material Design.
            </p>
          </div>
        </div>
      </div>
    </div>
  </Header>

  <div class="card card-body blur shadow-blur mx-3 mx-md-4 mt-n6">
    <PresentationCounter />
    <PresentationExample :data="data" />
  </div>
  <BackToTopButton />
  <DefaultFooter />
</template>

<script setup>
import {onMounted, onUnmounted} from 'vue'

//example components
import DefaultNavbar from '../../../examples/navbars/NavbarDefault.vue'
import DefaultFooter from '../../../examples/footers/FooterDefault.vue'

//image
import bg0 from '@/assets/img/bg9.jpg'

//sections
import Information from './Sections/AboutInformation.vue'

const body = document.getElementsByTagName('body')[0]
//hooks
onMounted(() => {
  body.classList.add('about-us')
  body.classList.add('bg-gray-200')
})

onUnmounted(() => {
  body.classList.remove('about-us')
  body.classList.remove('bg-gray-200')
})
</script>
<template>
  <DefaultNavbar
    :action="{
      route: 'javascript:;',
      label: 'Buy Now',
      color: 'btn-white',
    }"
    transparent
  />
  <header class="bg-gradient-dark">
    <div class="page-header min-vh-75" :style="{backgroundImage: `url(${bg0})`}">
      <span class="mask bg-gradient-dark opacity-6"></span>
      <div class="container">
        <div class="row justify-content-center">
          <div class="col-lg-8 text-center mx-auto my-auto">
            <h6 class="text-white mb-2 mt-5">Find me on</h6>
            <div class="d-flex justify-content-center">
              <a href="javascript:;"><i class="fab fa-twitter text-lg text-white me-4"></i></a>
            </div>
          </div>
        </div>
      </div>
    </div>
  </header>
  <div class="card card-body shadow-xl mx-3 mx-md-4 mt-n6">
    <Information />
  </div>
  <DefaultFooter />
</template>

<template>
    <div class="main-nav">
      <Link href="#">
        <i v-if="showIconsOnly" class="fa fa-home"></i>
        <span v-else>
          <i class="fa fa-home"></i> Home
        </span>
      </Link>
      <Link href="#">
        <i v-if="showIconsOnly" class="fa fa-question"></i>
        <span v-else>
          <i class="fa fa-question"></i> About Us
        </span>
      </Link>
      <Link href="#">
        <i v-if="showIconsOnly" class="fa-solid fa-cart-shopping"></i>
        <span v-else>
          <i class="fa-solid fa-cart-shopping"></i> Products
        </span>
      </Link>
      <Link href="#">
        <i v-if="showIconsOnly" class="fa-regular fa-images"></i>
        <span v-else>
          <i class="fa-regular fa-images"></i> Gallery
        </span>
      </Link>
      <Link href="#">
        <i v-if="showIconsOnly" class="fa-solid fa-phone-volume"></i>
        <span v-else>
          <i class="fa-solid fa-phone-volume"></i> Contact Us
        </span>
      </Link>
    </div>
  </template>
  
  <script setup>
  import { Link } from '@inertiajs/vue3';
  import { defineProps } from 'vue';
  
  // 'showIconsOnly' prop passed from the parent component
  const { showIconsOnly } = defineProps(['showIconsOnly']);
  </script>
  
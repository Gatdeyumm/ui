
  <script setup>
    import MainNav from '@/Components/MainNav.vue'
    import { ref } from 'vue';

    let width = ref('w-[250px]')
    let hidden = ref("")

    function toggleWidth() {
        if(width.value == 'w-[250px]') {
            width.value = 'w-[95px]'
            hidden.value = "hidden"
        }else {
            width.value = ['w-[250px]']
            hidden.value = ""
        }
    }
</script>

<template>

<div class="flex min-h-screen">
    <div id="sidebar" class="p-6 duration-500 bg-gray-900" :class="width" style="position: relative;">
        <button class="text-xl text-gray-600" @click="toggleWidth" style="position: absolute; right: 10px; top:10px">
            <i class="fa-solid fa-bars"></i>
        </button>

        <div id="branding" :class="hidden">
            <img src="https://i.pinimg.com/originals/8c/b2/9d/8cb29dcfb213a19e5e0e3f889e31df43.jpg" alt="Logo"
                class="w-[170px] h-[170px] mx-auto rounded-full object-cover">
            <h1 class="my-6 font-serif text-3xl text-center text-gray-200">Coco Chanel</h1>
            <hr class="border-gray-600">
        </div>

        <MainNav :showIconsOnly="hidden"></MainNav>
    
    </div>
    <div id="container" class="flex-1">
        <slot />
    </div>
    
</div>

</template>

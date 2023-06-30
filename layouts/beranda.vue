<template>
    <div class="min-h-screen duration-700 transition-all ease-out"
        :style="{ backgroundPosition: bgPos[0], backgroundSize: bgPos[1] }" style="  
            background-image: url('/bg/bg-comp1.png');
            background-color: rgb(248 250 252 / var(--tw-bg-opacity));
            background-repeat: no-repeat;
            ">
        <!-- index: backgroundSize-auto; backgroundPosition-center top -60px, kontak: backgroundSize-160em; backgroundPosition-center top -->
        <!-- <div class="h-20 w-full bg-orange-400 absolute top-0 z-10"></div> -->
        <div 
            :class="lokasiLogo" 
            class="flex items-end absolute transition-all duration-500 ease-in-out"
            >
            <img 
                src="/logo/cetakuy.png" 
                alt="" 
                :class="ukuranLogoDanText[0]"
                class="transition-all duration-500 ease-in-out">
            <h1 
                :class="ukuranLogoDanText[1]" 
                class="font-bold text-white transition-all duration-500 ease-in-out"
                >
                Cetakuy
            </h1>
        </div>

        <BerandaNavbar :lokasiGarisBawahNav="lokasiGarisBawahNav" :denganGarisBawahNav="denganGarisBawahNav" />
        <slot />
    </div>
</template>

<script setup>
const route = ref(useRoute())
console.log(route.value.name)
var bgPos = computed(() => {
    switch (route.value.name) {
        case 'index':
            return ['center top -90px', '100em']
        case 'daftar':
            return ['center top', '160em']
        default:
            return ['center top', '160em']
    }
})

var lokasiGarisBawahNav = computed(() => {
    return route.value.name == 'index'
})
var denganGarisBawahNav = computed(() => {
    return route.value.name == 'index' || route.value.name == 'kontak'
})
var lokasiLogo = computed(() => {
    switch (route.value.name) {
        case 'index':
            return 'top-20 left-20'
        case 'kontak':
            return 'top-2 left-6'
        case 'daftar':
            return "top-20 left-[38rem]"
    }
})
var ukuranLogoDanText = computed(() => {
    switch (route.value.name) {
        case 'index':
            return ['h-72', 'text-7xl -ml-6 mb-16 ']
        case 'kontak':
            return ['h-28', 'text-3xl -ml-2 mb-9']
        case 'daftar':
            return ['h-[14rem]', 'text-6xl -ml-6 mb-16 translate-y-[6.5rem] -translate-x-[12.5rem]']
    }
})

</script>
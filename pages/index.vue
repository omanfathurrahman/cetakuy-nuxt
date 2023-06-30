<template>
    <div class="" >
        <!-- <img src="/bg/bg-comp1.png" alt="" class="absolute -z-10 -top-20">  -->
        <div class="flex gap-12 px-12 pl-20">
            <div class="w-full pl-12">
                <div class="flex items-end opacity-0">
                    <img src="/logo/cetakuy.png" alt="" class="h-72 -ml-10">
                    <h1 class="text-7xl font-bold text-white -ml-6 mb-16">Cetakuy</h1>
                </div>
                <div class="flex flex-col gap-5 -mt-6">
                    <div class="flex flex-col gap-1 ">
                        <h3 class="text-4xl font-semibold text-white">Pesan online, bayar online<br>Lalu tunggu pesananmu di
                            rumah</h3>
                        <p class="text-white text-lg">Pesan di mana pun, bayar kapan pun</p>
                    </div>
                    <NuxtLink to="/daftar" class="w-fit text-lg text-white bg-orange-500 px-8 py-1.5 rounded-md font-semibold shadow-md">Daftar
                    </NuxtLink>
                </div>
            </div>
            <div class="w-2/3 flex items-end">
                <img src="/ilustrasi/ilustrasi1.png" alt="" class="h-fit">
            </div>
        </div>
        <div class="w-full mt-56 px-36">
            <h1 class="text-center mx-auto text-2xl font-semibold">Ayo Pesan Sekarang!</h1>
            <div class="grid grid-cols-4 gap-6 mt-6">
                <BerandaCardPromo />
                <BerandaCardPromo />
                <BerandaCardPromo />
                <BerandaCardPromo />
            </div>
        </div>
        <footer class="flex gap-3 items-center bg-stone-400/25 px-12 py-6 mt-12">
            <h3>Cetakuy 2023</h3>
        </footer>
    </div>
</template>

<script setup>
definePageMeta({
    layout: 'beranda',
});
</script>
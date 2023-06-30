<template>
    <div class="">
        <div class="flex gap-6 justify-end px-12 py-5">
            <div class="flex text-white relative">
                <div 
                    v-if="denganGarisBawahNav"
                    :class="lokasiGarisBawahNav? '-translate-x-[5.75rem]' : ''"
                    class="w-9 flex gap-1 absolute bottom-0 transition-all duration-700 ease-in-out right-8"
                    >
                    <div class="h-0.5 bg-white w-full rounded-full"></div>
                    <div class="h-0.5 bg-white w-1/3 rounded-full"></div>
                </div>
                <NuxtLink to="/" class="rounded-xl px-6 py-1.5">Home</NuxtLink>
                <NuxtLink to="/kontak" class="rounded-xl px-6 py-1.5">Kontak</NuxtLink>
            </div>
            <NuxtLink to="/auth/masuk" class="rounded-md px-8 py-1.5 bg-white text-orange-500 font-semibold">Masuk</NuxtLink>
        </div>
    </div>
</template>

<script setup>
defineProps({
    lokasiGarisBawahNav: Boolean,
    denganGarisBawahNav: Boolean
})
</script>
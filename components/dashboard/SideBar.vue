<template>
    <aside class="bg-stone-50 w-[266px] flex flex-col items-center gap-6 py-3 shadow-lg shadow-slate-400 z-20">
        <NuxtLink to="/" class="text-orange-500 text-[32px] font-bold">CetaKuy</NuxtLink>
        <div class="flex flex-col w-full px-6 gap-4">
            <NuxtLink 
                v-for="(page, index) in pages"
                :key="index"
                :to="page.path" 
                :class="[activePage == page.name ? 'text-orange-400 shadow-orange-300 border-orange-500' : 'text-neutral-400 shadow-slate-300 border-slate-500 hover:text-orange-300 hover:-translate-y-0.5 hover:border-orange-500 hover:border-opacity-25 hover:shadow-orange-200']"
                class="bg-stone-50 font-medium w-full py-2 text-center rounded-md shadow-lg ease-in duration-300 border border-opacity-25">
                {{ page.name }}
            </NuxtLink>
        </div>
    </aside>
</template>

<script setup>

const props = defineProps({
    pages: {
        type: Array,
        required: true
    },
    activePage: {
        type: String,
        required: true
    }
})
</script>
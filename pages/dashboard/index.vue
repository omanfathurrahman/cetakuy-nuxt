<template>
  <div class="px-16 py-7">
    <div class="h-full flex gap-7">
      <div 
        v-for="(menu, index) in menuPesanan"
        :key="index"
        class="w-full px-8 py-3 flex flex-col gap-2 rounded-lg bg-white shadow-md border"
        >
        <h2 class="text-xl font-semibold">{{ menu.judul }}</h2>
        <p>{{ menu.deskripsi }}</p>
        <div class="flex justify-end">
          <NuxtLink 
            :to="menu.link" 
            class="w-fit text-lg text-white bg-orange-500 px-8 py-1 rounded-md font-semibold shadow-md"
            >
            Pesan
          </NuxtLink>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
definePageMeta({
  layout: "dashboard",
  pageTransition: false,
  layoutTransition: false
});

const menuPesanan = [
  {
  'judul': 'Pesan Cetak',
  'deskripsi': 'Cetak dokumen, file atau desainmu sekarang',
  'link': '/pesan/cetak'
  },
  {
  'judul': 'Pesan Desain',
  'deskripsi': 'Belum punya desain? Yuk pesan sekarang',
  'link': '/pesan/desain'
  },
]

</script>
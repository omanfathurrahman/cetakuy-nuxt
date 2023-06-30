<template>
    <div class="flex flex-col justify-center items-center gap-12">
        <div class="flex flex-col items-center gap-6">
            <div class="flex flex-col items-center opacity-0">
                <img src="/logo/cetakuy.png" alt="">
                <h1 class="text-6xl font-bold text-white -mt-8">Cetakuy</h1>
            </div>
            <p class="text-white text-xl">Daftar sekarang yuk!</p>
        </div>
        <div class="flex gap-6 px-44">
            <div class="bg-white bg-opacity-90 gap-2.5 rounded-lg px-8 flex flex-col items-center text-center py-5">
                <h2 class="text-orange-500 font-semibold text-2xl">Daftar sebagai Customer</h2>
                <p>Rasakan nikmatnya memesan cetak tanpa mengantri, menunggu lama, pemesanan desain online, pembayaran
                    dengan paylater dan lain-lainnya</p>
                <NuxtLink to="/auth/daftar"
                    class="w-fit text-lg text-white bg-orange-500 px-8 py-1.5 rounded-md font-semibold shadow-md mt-2">Daftar
                </NuxtLink>
            </div>
            <div class="bg-white bg-opacity-90 gap-2.5 rounded-lg px-8 flex flex-col items-center text-center py-5">
                <h2 class="text-orange-500 font-semibold text-2xl">Daftar sebagai Freelancer Desain</h2>
                <p>Jadilah mitra kami dan peroleh keuntungan lebih. Terima pesanan dari CetaKuy tanpa perlu bertemu langsung dengan clien</p>
                <NuxtLink to="/auth/daftar"
                    class="w-fit text-lg text-white bg-orange-500 px-8 py-1.5 rounded-md font-semibold shadow-md mt-2">Daftar
                </NuxtLink>
            </div>
        </div>
        
    </div>
</template>

<script setup>
definePageMeta({
    layout: 'beranda'
})
</script>
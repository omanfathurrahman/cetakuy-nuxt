<template>
    <div 
        style="background-image: url('/bg/bg4.png');"
        class="h-screen w-screen flex items-center justify-center"
        >
        <div class="bg-white rounded-xl flex flex-col items-center w-2/3">
            <div class="">
                <img 
                    src="/logo/cetakuy.png" 
                    class="w-32"
                    >
            </div>
            <div class="border border-r-0 border-l-0 flex w-full py-5">
                <div class="flex flex-col gap-2 w-1/3 px-12 border-r">
                    <div 
                        v-for="(item, index) in dataPembeli"
                        :key="index"
                        class="">
                        <h3 class="text-lg font-medium">{{ item }}</h3>
                        <p>Tatang Suratang</p>
                    </div>
                </div>
                <div class="w-full px-4">
                    <table class="w-full">
                        <tr class="text-center border-b">
                            <th
                                v-for="(item, index) in dataHeadBarangDibeli"
                                :key="index"
                                >{{ item }}</th>
                        </tr>
                        <tr class="text-center">
                            <td>Ikan Bakar</td>
                            <td>Ikan Bakar</td>
                            <td>Ikan Bakar</td>
                            <td>Ikan Bakar</td>
                        </tr>
                    </table>
                </div>
            </div>
            <div class="flex justify-between px-16 py-6 w-full">
                <button class="w-fit text-lg text-slate-500 bg-white border px-8 py-1 rounded-md font-semibold shadow-md">Kembali</button>
                <button class="w-fit text-lg text-white bg-orange-500 px-8 py-1 rounded-md font-semibold shadow-md">Confirm</button>
            </div>
        </div>
    </div>
</template>

<script setup>
definePageMeta({
  layout: "default",
  pageTransition: false,
  layoutTransition: false
});

const dataPembeli = ['Nama', 'Email', 'Penerima', 'No Whatsapp Penerima']
const dataHeadBarangDibeli = ['Item', 'Harga Satuan', 'Jumlah', 'Subtotal']
</script>
<template>
    <div class="pl-10 pr-16 py-8">
        <div class="flex flex-col gap-2 bg-white rounded-lg px-8 py-4">
            <h1 class="text-orange-500 font-semibold text-xl">Pesan Desain</h1>
            <div class="flex items-end gap-8">
                <div class="w-full flex flex-col gap-2">
                    <div class="flex flex-col gap-1 w-full">
                        <label for="" class="font-md text-base text-slate-700">
                            Nama Pesanan
                        </label>
                        <input type="text" name="" id=""
                            class="w-full border border-slate-300 rounded-md py-0.5 focus:outline-none">
                    </div>
                    <div class="flex flex-col gap-1 w-full">
                        <label for="deskripsi" class="font-md text-base text-slate-700">
                            Deskripsi
                        </label>
                        <textarea type="text" name="deskripsi" id="deskripsi"
                            class="w-full border border-slate-300 rounded-md text-slate-700 focus:outline-none px-2 py-1 resize-none h-fit"></textarea>
                    </div>
                    <div class="flex flex-col gap-1 w-full">
                        <label for="" class="font-md text-base text-slate-700">
                            Jenis Desain
                        </label>
                        <input type="text" name="" id=""
                            class="w-full border border-slate-300 rounded-md py-0.5 focus:outline-none">
                    </div>
                    <div class="flex flex-col gap-1 w-full text-slate-800">
                        <label for="ukuran" class="font-md text-base text-slate-700">
                            Ukuran
                        </label>
                        <div class="flex gap-8">
                            <select name="pilih-ukuran" id=""
                                class="text-slate-800 w-full border border-slate-300 rounded-md py-0.5 px-3">
                                <option value="a4">A4</option>
                                <option value="a3">A3</option>
                                <option value="a2">A2</option>
                            </select>
                            <div class="flex gap-2 items-center ">
                                <input type="number" name="panjang" id=""
                                    class="border border-slate-300 rounded-md py-0.5 w-20 text-center focus:outline-none"
                                    placeholder="Panjang">
                                <span class="text-slate-800">X</span>
                                <input type="number" name="tinggi" id=""
                                    class="border border-slate-300 rounded-md py-0.5 w-20 text-center focus:outline-none"
                                    placeholder="Tinggi">
                            </div>
                            <select name="satuan-ukuran" id=""
                                class="border border-slate-300 rounded-md py-0.5 w-20 text-center text-slate-800">
                                <option value="px">px</option>
                                <option value="cm">cm</option>
                                <option value="m">m</option>
                            </select>
                        </div>
                    </div>
                    <div class="flex flex-col gap-1 w-full">
                        <label for="" class="font-md text-base text-slate-700">
                            Referensi
                        </label>
                        <input type="text" name="" id=""
                            class="w-full border border-slate-300 rounded-md py-0.5 focus:outline-none">
                    </div>
                    <div class="flex flex-col gap-1 w-full">
                        <label for="" class="font-md text-base text-slate-700">
                            Unggah file
                        </label>
                        <input type="text" name="" id=""
                            class="w-full border border-slate-300 rounded-md py-0.5 focus:outline-none">
                    </div>
                </div>
                <NuxtLink to="/checkout" class="rounded-md bg-orange-500 text-white px-5 py-1 h-fit">Pesan</NuxtLink>
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
</script>
<template>
    <div class="w-screen h-screen px-16 py-10 object-cover" style="background-image: url('/bg/bg3.png');">
        <div class="w-full h-full flex gap-20 items-center">
            <div class="h-full w-full px-10 flex flex-col gap-6">
                <img src="/logo/cetakuy.png" alt="" class="w-3/12 mx-auto">
                <div class="flex flex-col gap-3">
                    <h2 class="text-4xl font-semibold">Cetak atau Pesan Desain kapanpun dimanapun</h2>
                    <p class="text-lg">Efisienkan waktumu dengan mencetak sesuatu tanpa perlu ke tempat percetakan terlebih dahulu</p>
                </div>
                <div class="flex flex-col gap-1">
                    <h3 class="font-semibold text-xl">Punya bakat desain? ingin mendapatkan penghasilan tambahan?</h3>
                    <p>Yuk daftar sebagai freelancer desain di CetaKuy!</p>
                    <button class="bg-white text-orange-500 px-6 py-1.5 rounded-lg border border-orange-500 w-fit">Daftar sebagai freelancer</button>
                </div>
                <div class="flex flex-col gap-1">
                    <h3 class="font-semibold text-xl">Anda pengelola tempat percetakan? ayo daftarkan tempat percetakanmu di CetaKuy!</h3>
                    <p>Hubungi admin untuk mendaftarkan tempat percetakan</p>
                    <button class="bg-white text-orange-500 px-6 py-1.5 rounded-lg border border-orange-500 w-fit">Hubungi admin</button>
                </div>
            </div>
            <div class="h-fit w-full bg-white rounded-3xl shadow-lg flex flex-col items-center px-16 py-10 border gap-2.5">
                <div class="flex flex-col gap-2 items-center">
                    <h1 class="text-4xl font-semibold">Buat Akun</h1>
                </div>
                <div class="flex flex-col gap-2 items-center w-full text-neutral-500">

                    <form class="w-full">
                        <div class="w-full flex flex-col gap-1">
                            <p>Nama Depan</p>
                            <input 
                                v-model="namaDepan"
                                type="text" 
                                name="" 
                                id="nama-depan" 
                                class="outline-none bg-white px-4 py-1.5 rounded-lg border border-orange-500 w-full"
                                required
                            >
                        </div>
                        <div class="w-full flex flex-col gap-1">
                            <p>Nama Belakang</p>
                            <input 
                                v-model="namaBelakang"
                                type="text" 
                                name="" 
                                id="nama-belakang" 
                                class="outline-none bg-white px-4 py-1.5 rounded-lg border border-orange-500 w-full"
                                required
                            >
                        </div>
                        <div class="w-full flex flex-col gap-1">
                            <p>Email</p>
                            <input 
                                v-model="email"
                                type="email" 
                                name="" 
                                id="email" 
                                class="outline-none bg-white px-4 py-1.5 rounded-lg border border-orange-500 w-full"
                                required
                            >
                        </div>
                        <div class="w-full flex flex-col gap-1">
                            <p>Password</p>
                            <input 
                                v-model="password"
                                type="password" 
                                name="" 
                                id="password" 
                                class="outline-none bg-white px-4 py-1.5 rounded-lg border border-orange-500 w-full"
                                required
                            >
                        </div>
                        <div class="w-full flex flex-col gap-1">
                            <p>Konfirmasi password</p>
                            <input 
                                type="password" 
                                name="" 
                                id="val-password" 
                                class="outline-none bg-white px-4 py-1.5 rounded-lg border border-orange-500 w-full"
                                required
                            >
                        </div>
                        <div class="flex w-full">
                            <p>Sudah punya akun? <NuxtLink to="/auth/masuk" class="text-orange-500">Masuk</NuxtLink></p>
                        </div>
                        <input type="submit" @click="daftar" class="mt-2 bg-orange-500 shadow-md text-white font-medium px-6 py-1.5 rounded-lg border border-orange-500 w-full text-center" value="Daftar" />
                    </form>
                </div>
                <div class="flex items-center gap-3 w-full">
                    <div class="w-full h-0.5 bg-orange-400"></div>
                    <p class="min-w-max text-neutral-400">Atau masuk dengan</p>
                    <div class="w-full h-0.5 bg-orange-400"></div>
                </div>
                <div class="flex gap-2 w-full">
                    <div class="border border-orange-400 rounded-lg py-2 text-center text-orange-400 bg-white w-full">Google</div>
                    <div class="border border-orange-400 rounded-lg py-2 text-center text-orange-400 bg-white w-full">Facebook</div>
                </div>
                <div class=" text-neutral-400">
                    <p>Dengan melakukan pendaftaran, kamu setuju dengan <a href="#" class="text-orange-500">syarat penggunaan</a> dan <a href="#" class="text-orange-500">kebijakan privasi</a></p>
                </div>
            </div>
        </div>
    </div>
</template>

<script setup>
const namaDepan = ref("")
const namaBelakang = ref("")
const email = ref("")
const password = ref("")
const valpassword = ref("")



async function daftar() {
    var data = {
        'namaDepan': namaDepan.value,
        'namaBelakang':namaBelakang.value,
        'email':email.value,
        'password':password.value,

    }
    console.log(data)
    await fetch('http://127.0.0.1:5000/users', {
        method: 'POST',
        headers: {
            'Content-Type': 'application/json'
        },
        body: JSON.stringify(data)
    });
    console.log(namaDepan)
    console.log(namaBelakang)
    if ( namaDepan.value != "" && namaBelakang.value != "" && email.value != "" && password.value != "" && valpassword.value != "") {
        navigateTo('/auth/verifikasi')
    }
}
</script>
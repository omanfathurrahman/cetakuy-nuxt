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
            <div class="flex flex-col gap-2 items-center w-full text-neutral-900">

                    <form class="w-full" @submit.prevent="daftar()">
                        <p 
                            class="text-red-600 text-center"
                            v-if="emailSudahDipakai"
                            >
                        Email sudah digunakan
                    </p>
                        <p 
                            class="text-red-600 text-center"
                            v-if="passwordTidakSama"
                            >
                        Password dan validasi password tidak sama
                    </p>
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
                                v-model="valpassword"
                                type="password" 
                                name="" 
                                id="val-password" 
                                class="outline-none bg-white px-4 py-1.5 rounded-lg border border-orange-500 w-full"
                                required
                            >
                    </div>
                    <div class="flex w-full">
                        <p class="text-neutral-500">Sudah punya akun? <NuxtLink to="/auth/masuk" class="text-orange-500">Masuk</NuxtLink>
                        </p>
                    </div>
                    <!-- <button type="submit" class="mt-2 bg-orange-500 shadow-md text-white font-medium px-6 py-1.5 rounded-lg border border-orange-500 w-full text-center">Daftar</button> -->
                    <button type="submit" class="mt-2 bg-orange-500 shadow-md text-white font-medium px-6 py-1.5 rounded-lg border border-orange-500 w-full text-center flex justify-center">
                        <img v-if="sedangLoading" src="/animasi/loading.svg" alt="" class="h-7">
                        <p v-else>Daftar</p>
                    </button>
                    <!-- <input type="submit" class="mt-2 bg-orange-500 shadow-md text-white font-medium px-6 py-1.5 rounded-lg border border-orange-500 w-full text-center" value="Daftar" /> -->
                    <!-- <input 
                            type="submit" 
                            class="mt-2 bg-orange-500 shadow-md text-white font-medium px-6 py-1.5 rounded-lg border border-orange-500 w-full text-center" 
                            value="Daftar" 
                        /> -->
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
const namaDepan = ref("first name")
const namaBelakang = ref("last name")
const email = ref("example@email.com")
const password = ref("123")
const valpassword = ref("123")

const sedangLoading = ref(false)
const passwordTidakSama = ref(false)
const emailSudahDipakai = ref(false)

async function daftar() {
    if (password.value != valpassword.value) {
        passwordTidakSama.value = true
        setTimeout(() => {
            passwordTidakSama.value = false;
        }, 6000)
        return
    }

    if (namaDepan.value != "" && namaBelakang.value != "" && email.value != "" && password.value != "" && valpassword.value != "") {
        console.log(namaDepan.value, namaBelakang.value, email.value, password.value, valpassword.value)
        sedangLoading.value = true
        setTimeout(() => {
            sedangLoading.value = false;
            navigateTo("/auth/verifikasi")
        }, 5000)
    }
}

// async function daftar() {
//     if (password.value != valpassword.value) {
//         passwordTidakSama.value = true
//         setTimeout(() => {
//           passwordTidakSama.value = false;
//         }, 6000)
//         return
//     }

//     const data2 = await fetch('http://127.0.0.1:5000/users')
//     var data3 = await data2.json()

//     // console.log( typeof data3.user)
//     // console.log(data3.user)

//     for (let i in data3.user) {
//         console.log(data3.user[i].email)
//         if (data3.user[i].email == email.value) {
//             emailSudahDipakai.value = true
//             setTimeout(() => {
//                 emailSudahDipakai.value = false;
//             }, 6000)
//             return
//         }
//     }

//     var data = {
//         'namaDepan': namaDepan.value,
//         'namaBelakang':namaBelakang.value,
//         'email':email.value,
//         'password':password.value,

//     }
//     const res = await fetch('http://127.0.0.1:5000/users', {
//         method: 'POST',
//         headers: {
//             'Content-Type': 'application/json'
//         },
//         body: JSON.stringify(data)
//     });

//     const resData = await res.json()
//     console.log(resData)
//     if ( namaDepan.value != "" && namaBelakang.value != "" && email.value != "" && password.value != "" && valpassword.value != "") {
//         console.log(namaDepan.value, namaBelakang.value, email.value, password.value, valpassword.value)
//         sedangLoading.value = true
//         setTimeout(() => {
//                 sedangLoading.value = false;
//                 navigateTo("/auth/verifikasi")
//         }, 5000)
//     }
// }
</script>

<template>
    <div class="w-screen h-screen flex justify-center items-center" style="background-image: url('/bg/bg.png');">
        <div class="flex flex-col items-center w-full text-neutral-400 gap-3 -mt-10">
            <div class="flex flex-col items-center font-semibold text-orange-500">
                <img src="/logo/cetakuy.png" alt="" class="w-[170px] h-[170px]">
                <h1 class="text-3xl -mt-5">Masuk</h1>
            </div>
            <div class="w-3/12 flex flex-col gap-1.5">
                <div class="flex flex-col items-center gap-2">
                    <div class="flex flex-col gap-3 w-full">
                        <input class="border border-orange-500 w-full px-4 py-2 rounded-lg outline-none" type="email" name="" id=""
                            placeholder="Email">
                        <input class="border border-orange-500 w-full px-4 py-2 rounded-lg outline-none" type="password" name="" id=""
                            placeholder="Password">
                    </div>
                    <div class="flex justify-between w-full">
                        <div class="flex gap-2">
                            <p>Belum punya akun?</p>
                            <NuxtLink to="/auth/daftar" class="text-orange-500">Daftar</NuxtLink>
                        </div>
                        <a href="#">Lupa password?</a>
                    </div>
                    <NuxtLink to="/dashboard" class="w-full bg-orange-500 text-center py-2 rounded-lg text-white font-medium">Masuk</NuxtLink>
                </div>
                <div class="flex items-center gap-3">
                    <div class="w-full h-0.5 bg-orange-500"></div>
                    <p class="min-w-max">Atau masuk dengan</p>
                    <div class="w-full h-0.5 bg-orange-500"></div>
                </div>
                <div class="flex gap-2">
                    <div class="border border-orange-500 rounded-lg py-2 text-center text-orange-500 bg-white w-full">Google</div>
                    <div class="border border-orange-500 rounded-lg py-2 text-center text-orange-500 bg-white w-full">Facebook</div>
                </div>
            </div>
        </div>
    </div>
</template>

<script setup>

</script>
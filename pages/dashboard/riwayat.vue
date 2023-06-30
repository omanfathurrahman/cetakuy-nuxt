<template>
  <div class="pl-10 pr-16 py-8">
    <div class="bg-white px-8 py-6 rounded-lg grid grid-cols-2 gap-3 shadow-md">
      <div 
        v-for="(_, index) in [...Array(5).keys()]"
        class="border rounded-lg px-8 py-2">
        <h3 class="text-xl">Cetak Baliho Politik</h3>
        <div class="flex flex-col gap-2 mt-2">
          <table class="">
            <tr class="">
              <th class="text-left">Tanggal Pemesanan</th>
              <td class="">:</td>
              <td class="text-right">xx-yy-zzzz</td>
            </tr>
            <tr class="">
              <th class="text-left">Diproses oleh</th>
              <td class="">:</td>
              <td class="text-right">Percetakan OnlyCetak</td>
            </tr>
            <tr class="">
              <th class="text-left">Diselesaikan pada</th>
              <td class="">:</td>
              <td class="text-right">xx-yy-zzzz</td>
            </tr>
          </table>
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
</script>
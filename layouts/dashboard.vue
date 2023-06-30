<template>
    <div class="flex h-screen" style="background-image: url('/bg/bg2.png');">
        <DashboardSideBar 
            :pages="pages" 
            :active-page="activePage()"
            />
        <div class="w-full flex flex-col">
            <DashboardTopBar 
                :active-page="activePage()"
                />
            <slot />
        </div>
    </div>
</template>

<script setup>
const pages = [
    {
        name: 'Pesan',
        path: '/dashboard'
    },
    {
        name: 'Pengerjaan',
        path: '/dashboard/pengerjaan'
    },
    {
        name: 'Riwayat',
        path: '/dashboard/riwayat'
    }]

    
const route = useRoute()

function activePage() {
    switch (route.name) {
        case 'dashboard':
            return 'Pesan'
        case 'dashboard-pengerjaan':
            return 'Pengerjaan'
        case 'dashboard-riwayat':
            return 'Riwayat'
        default:
            return 'Pesan'
    }
}
    


</script>
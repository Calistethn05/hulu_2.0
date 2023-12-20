
import type HeaderItemVue from './HeaderItem.vue';
<template>
    <header class="flex flex-col sm:flex-row m-5 justify-between items-center">
        <ul class="flex flex-grow justify-evenly max-w-2xl">
            <HeaderItem v-for="link of links" :key="link.title"
            :title= "link.title" 
            :Icon="link.icon" />
        </ul>
        <img src="../assets/ua6.webp" alt="Logo Hulu">
    </header>
</template>

<script setup lang="ts">
import HeaderItem from "@/components/HeaderItem.vue";
import { 
    HomeIcon,
    BoltIcon,
    CheckBadgeIcon,
    RectangleStackIcon,
    MagnifyingGlassIcon,
    UserIcon,
 } from "@heroicons/vue/24/outline";

 const links = [
    {title: "home", icon: HomeIcon },
    {title: "Trending", icon: BoltIcon },
    {title: "Verified", icon: CheckBadgeIcon },
    {title: "Collections", icon: RectangleStackIcon },
    {title: "Search", icon: MagnifyingGlassIcon },
    {title: "Account", icon: UserIcon }
 ];
</script>
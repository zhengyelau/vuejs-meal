<template>
    <!-- <h1 class="bg-blue-500">App.vue</h1> -->
    <div class="bg-gray-100 h-full">
        <NavBar />
        <main>
            <router-view />
        </main>
    </div>
</template>

<script setup>
import NavBar from "./Navbar.vue"
</script>
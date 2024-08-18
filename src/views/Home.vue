<script setup>
import { computed } from 'vue';
import store from "../store"
const meal = computed(() => store.state.meals)

const letters = "ABCDEFGHIJKLMNOPQRSTUVWXYZ"

</script>

<template>
    <div class="flex flex-col p-8">

        <div>
            <input type="text" class="rounded border-2 border-gray-200 w-full" placeholder="Search for meals" />
        </div>

        <div class="flex gap-2 mt-2 justify-center">
            <router-link :to="{name: 'byLetter', params: {letter: letter}}" v-for="letter in letters.split('')" :key="letter">
                {{ letter }}
            </router-link>
        </div>
    </div>
</template>
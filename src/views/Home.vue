<script setup>
import { computed, onMounted, ref } from 'vue';
import store from "../store"
import axiosClient from "../axiosClient"
const meal = computed(() => store.state.meals)

const letters = "ABCDEFGHIJKLMNOPQRSTUVWXYZ"
const ingredients = ref([]);
onMounted(async() => {
    await axiosClient.get('list.php?i=list').then((res) => {
        ingredients.value = res.data
    })
})

</script>

<template>
    <div class="flex flex-col p-8 h-full">



        <div class="flex gap-2 mt-2 justify-center">
            <router-link :to="{name: 'byLetter', params: {letter: letter}}" v-for="letter in letters.split('')" :key="letter">
                {{ letter }}
            </router-link>
        </div>
    </div>
</template>
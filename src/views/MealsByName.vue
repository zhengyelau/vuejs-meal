<script setup>
import { computed, ref } from 'vue';
import axiosClient from '../axiosClient';
import store from '../store/index';

const keyword = ref('');
const meals = computed(() => store.state.searchedMeals)

const searchMealss = () => {
    store.dispatch('searchMeals', keyword.value)
}

</script>

<template>
    <div class="p-8">
        <input type="text" @change="searchMealss" v-model="keyword" class="rounded border-2 border-gray-200 w-full" placeholder="Search for meals" />
    </div>

    <pre>{{ meals }}</pre>
</template>
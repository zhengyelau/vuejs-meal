<script setup>
import { computed } from 'vue';
import store from "../store"
const meal = computed(() => store.state.meals)
</script>

<template>
    Home
    <pre>{{ meal }}</pre>
</template>
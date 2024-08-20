<template>
    <header class="bg-white shadow h-16 flex justify-between items-stretch">
        <router-link :to="{ name: 'home' }" class="inline-flex items-center h-full px-5">Home</router-link>
        <div class="flex gap-1 items-center">
            <router-link :to="{ name: 'byName' }"
                class="px-2 h-full hover:bg-purple-100 inline-flex items-center transition-color">Search
                Meal</router-link>
            <router-link :to="{ name: 'byLetter' }"
                class="px-2 h-full hover:bg-purple-100 inline-flex items-center transition-color">Meals By
                letter</router-link>
            <router-link :to="{ name: 'byIngredient' }"
                class="px-2 h-full hover:bg-purple-100 inline-flex items-center transition-color">Meals by
                gradients</router-link>
        </div>
    </header>
</template>
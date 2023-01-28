
import ComponentA from './componentA.vue';


import { component } from 'vue/types/umd';


<template>
    <div class="border1px">
        <p>Component A and B in component C</p>
        <componentA />
        <componentB />
    </div>
</template>

<style scoped>
    .border1px{
        border: 1px solid red;
    }
</style>
<template>
    <label>A</label>
    <input v-model="a" type="number"/>

    <label>B</label>
    <input v-model="b" type="number"/>

    <label>C</label>
    <p>{{ c }}</p>

    <label>Opération</label>
    <select v-model="operator">
        <option value="+">+</option>
        <option value="-">-</option>
        <option value="*">*</option>
        <option value="/">/</option>
    </select>

    <button @click="calculate">Calculate</button>
</template>

<script setup>

import { ref } from 'vue';

const a = ref();
const b = ref();
const c = ref();

const operator = ref();

const calculate = () => {
    switch(operator.value) {
        case "+": 
            c.value = Number(a.value) + Number(b.value);
            break;
        case "-": 
            c.value = Number(a.value) - Number(b.value);
            break;
        case "*":
            c.value = Number(a.value) * Number(b.value);
            break;
        case "/":
            c.value = Number(a.value) / Number(b.value);
            break;
    }
}

</script>
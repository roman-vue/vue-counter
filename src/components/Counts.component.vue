<template>
    <h1>Counter</h1>
    <h3>{{ number }}</h3>
    <button class="add" @click="addValue">➕</button>
    <button class="minus" @click="minusValue">➖</button>
</template>

<script>
import { ref } from "@vue/reactivity";
export default {
    setup() {
        const number = ref(0);
        const addValue = () => {
            number.value++;
        };

        const minusValue = () => {
            number.value--;
        };

        return {
            number: number,
            addValue,
            minusValue,
        };
    },
};
</script>

<style len="sass">
.add {
    background-color: rgb(166, 248, 166);
    width: 20vh;
    border-radius: 10vh;
}

.minus {
    background-color: rgb(255, 140, 140);
    width: 20vh;
    border-radius: 10vh;
}
</style>

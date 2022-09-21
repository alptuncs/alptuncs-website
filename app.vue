<script setup lang="ts">

    const counterState = reactive({
        counter: 0,
    });
</script>

<template>
    <div class="container">
        <h1 class="website-title">Welcome</h1>
        <div>
            <h3 class="info">You have clicked the button  {{counterState.counter}}  times</h3>
        </div>
        <div class="button-container">
            <button class="interactive-button"
                    @click="counterState.counter += 1">
                Increase
            </button>
            <button class="interactive-button"
                    @click="counterState.counter -= 1">
                Decrease
            </button>
            <button class="interactive-button"
                    @click="counterState.counter = 0">
                Reset
            </button>
        </div>
        <h1><nuxt-link to:"/about">About</nuxt-link></h1>
    </div>
</template>

<style scoped>
    .container {
        text-align: center;
    }

    .website-title {
        font-family: Arial, Helvetica, sans-serif;
        color: rgb(50,50,256);
        text-align: center;
    }

    .info {
        font-family: Arial,Arial, Helvetica, sans-serif;
        text-align: center;
    }

    .button-container {
        position: relative;
    }

    .interactive-button {
        text-align: center;
    }
</style>

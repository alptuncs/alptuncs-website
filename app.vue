<script setup lang="ts">

    const counterState = reactive({
        counter: 0,
    });
</script>

<template>
    <div>
        <h1>Welcome</h1>
        <div>
            <h3>You have clicked the button  {{counterState.counter}}  times</h3>
        </div>
        <div>
            <button @click="counterState.counter += 1">
                Increase
            </button>
            <button @click="counterState.counter -= 1">
                Decrease
            </button>
            <button @click="counterState.counter = 0">
                Reset
            </button>
        </div>
    </div>
</template>

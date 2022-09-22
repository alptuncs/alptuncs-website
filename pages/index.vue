<template>
  <div class="container">
    <h1>Hello, you have clicked the button: {{this.$store.state.counterStore.counter}} times</h1>
    <div class="space">
      <button class="button"
              @click="increasevalue">
        Click
      </button>
      <button class="button"
              @click="reset">
        Reset
      </button>
    </div>
  </div>
</template>

<script>
  export default {
    methods: {
      increasevalue() {
        this.$store.commit('counterStore/increment')
      },
      reset() {
        this.$store.commit('counterStore/reset')
      }
    },
  }
</script>

<style>
  .container {
    text-align: center;
    padding-top: 30px;
  }

  .space {
    height: auto;
    text-align: center;
  }

  .button {
    padding: 4px;
    background: #808080b2;
    border-radius: 10px;
    color: white;
  }
</style>

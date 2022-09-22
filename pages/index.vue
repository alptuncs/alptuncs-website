<template>
  <div class="container">
    <h1>Hello You have clicked the button: {{this.$store.state.counterStore.counter}} times</h1>
    <div class="space">
      <button class="helloButton"
              @click="increasevalue">
        Click
      </button>
    </div>
  </div>
</template>

<script>
  export default {
    methods: {
      increasevalue() {
        this.$store.commit('counterStore/increment')
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

  .helloButton {
    padding: 4px;
    background: #808080b2;
    border-radius: 10px;
  }
</style>

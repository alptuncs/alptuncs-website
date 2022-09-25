<template>
  <div>
    <div class="title">
      <h1>Hello, you have clicked the button {{this.$store.state.counterStore.counter}} times</h1>
    </div>
    <div class="buttonContainer">
      <v-btn @click="increasevalue">Click</v-btn>
      <v-btn @click="reset">Reset</v-btn>
    </div>
    <gallery></gallery>
  </div>
</template>

<script>
  import gallery from '~/components/gallery.vue'
  export default {
    components: {
      gallery
    },
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
  .title {
    height: 100px;
    text-align: center;
    padding-top: 20px;
  }

  .buttonContainer {
    text-align: center;
  }
</style>

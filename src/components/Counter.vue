<template>
  <div>
    <button @click="increasein">+</button>
    <button @click="decreasein">-</button>
    <p>{{num}}</p>
  </div>
</template>

<script>
export default {
  name: 'Counter',
  props: {
    num: {
      type: Number,
      default: 0
    }
  },
  // data () {
  //   return {
  //     num: 0
  //   }
  // },
  methods: {
      increasein() {
        this.$emit('increase');
      },
      decreasein() {
        this.$emit('decrease');
      }
  }
}
</script>

<style>
</style>

<template>
  <div>
    <p>
      <input type="text" v-model="greetings">
    </p>
    <p>
      {{ greetings }} ({{ greetings.length }})
    </p>
  </div>
</template>

<script>
export default {
  name: "app",
  data() {
    return {
      greetings: 'Nuxt 3'
    }
  },
  mounted() {
    setTimeout(() => {
      this.greetings = 'Nuxt 3 Absolute Basics'
    }, 3000)
  }
}
</script>

<style scoped>

</style>
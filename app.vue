<template>
  <div>
    <button :class="active ? 'text-red' : 'text-green'" @click="toggle">Click Me</button>
  </div>
</template>

<script>
export default {
  name: "app",
  data() {
    return {
      active: false
    }
  },
  methods: {
    toggle() {
      this.active = ! this.active
    }
  }
}
</script>

<style scoped>
.text-green {
  color: green;
}
.text-red {
  color: red;
}
</style>
<template>
  <div>
    <button :class="{
      'button' : true,
      'text-primary' : type === 'primary',
      'text-secondary' : type === 'secondary'
    }">
      <slot/>
    </button>
  </div>
</template>

<script>
export default {
  name: "ButtonComponent",
  props: {
    type: {
      type: String,
      default: "primary"
    }
  }
}
</script>

<style scoped>
.button {
  background: white;
  padding: 5px 15px;
  border-radius: 5px;
}

.text-primary {
  color: blue;
}

.text-secondary {
  color: green;
}
</style>
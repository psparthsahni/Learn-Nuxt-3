<template>
  <div>
    <ButtonComponent type="primary">
      Hello World
    </ButtonComponent>
  </div>
</template>

<script>
import ButtonComponent from "./components/ButtonComponent";

export default {
  name: "app",
  components: {
    ButtonComponent,
  }

}
</script>

<style scoped>

</style>
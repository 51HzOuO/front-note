<script>
export default {
  data() {
    return {}
  },
  name: "Test02",
  props: {
    message: {
      type: String,
      default: "Test02 页面"
    }
  },
  methods: {
    handleClick() {
      this.$emit("change", "Test02 页面");
    }
  }
}
</script>

<template>
  <div>
    <h1>
      {{ message }}
    </h1>
  </div>
</template>

<style scoped lang="scss">
div {
  display: flex;
  justify-content: center;
}
</style>

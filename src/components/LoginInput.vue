<template>
  <label>
    {{ label }}
    <input type="text" v-model="inputValue" />
  </label>
</template>

<script>
export default {
  name: "LoginInput",
  props: ['label', 'modelValue'], 
  computed: {
    inputValue: {
      get() {
        return this.modelValue;
      },
      set(value) {
        this.$emit("update:modelValue",value);
      },
    },
  },
};
</script>
<style scoped>
input {
  display: block;
}
</style>
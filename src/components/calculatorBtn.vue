<template>
  <button class="calculatorBtn" @click="emitBtnClick">{{value}}</button>
</template>

<script>
export default {
  name: "my-button",
  props: {
    value: [String, Number]
  },
  methods: {
    emitBtnClick() {
      this.$emit('btnClick', this.value);
    }
  }
}
</script>

<style scoped>
.calculatorBtn {
  display: block;
  font-family: sans-serif;
  font-size: 20px;
  color: rgb(255, 255, 255);
  background-color: rgb(30, 30, 30);
  border: none;
}
</style>
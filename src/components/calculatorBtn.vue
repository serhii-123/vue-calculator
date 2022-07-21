<template>
  <button class="calculatorBtn" @click="emitBtnClick">{{symbol}}</button>
</template>

<script>
export default {
  name: "my-button",
  props: {
    symbol: [String, Number]
  },
  methods: {
    emitBtnClick() {
      this.$emit('btnClick', this.symbol);
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
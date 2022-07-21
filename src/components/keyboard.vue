<template>
  <div class="keyboard">
    <calculator-btn
        class="keyboard__btn"
        v-for="value in symbols"
        :symbol="value"
        @btn-click="handleClick"
    ></calculator-btn>
  </div>
</template>

<script>
import CalculatorBtn from '@/components/calculatorBtn'

export default {
  name: "keyboard",
  components: {
    CalculatorBtn
  },
  data() {
    return {
      symbols: ['1', '2', '3', '4', '5', '6', '7', '8', '9', '0', '+', '-', '*', '/', '(', ')', '=']
    };
  },
  methods: {
    handleClick(e) {
      alert(e);
    }
  }
}
</script>

<style scoped>
.keyboard {
  display: flex;
  flex-wrap: wrap;
}
.keyboard__btn {
  width: 74px;
  height: 74px;
  margin: 0 8px 8px 0;
}
.keyboard__btn:nth-child(4n) {
  margin: 0 0 8px 0;
}
.keyboard__btn:last-child {
  width: 100%;
  margin: 0;
}
</style>
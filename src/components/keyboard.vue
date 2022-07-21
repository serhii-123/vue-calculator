<template>
  <div class="keyboard">
    <calculator-btn
        v-for="n in 9"
        :symbol="n"
        @btn-click="handleClick"
    ></calculator-btn>
    <calculator-btn symbol="0"></calculator-btn>
    <calculator-btn symbol="+"></calculator-btn>
    <calculator-btn symbol="-"></calculator-btn>
    <calculator-btn symbol="*"></calculator-btn>
    <calculator-btn symbol="/"></calculator-btn>
    <calculator-btn symbol="("></calculator-btn>
    <calculator-btn symbol=")"></calculator-btn>
    <calculator-btn symbol="="></calculator-btn>
  </div>
</template>

<script>
import CalculatorBtn from '@/components/calculatorBtn'

export default {
  name: "keyboard",
  components: {
    CalculatorBtn
  },
  methods: {
    handleClick(e) {
      alert(e);
    }
  }
}
</script>

<style scoped>

</style>
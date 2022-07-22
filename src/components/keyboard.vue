<template>
  <div class="keyboard">
    <calculator-btn
        class="keyboard__btn"
        v-for="value in values"
        :value="value"
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
      values: ['1', '2', '3', '4', '5', '6', '7', '8', '9', '0', '+', '-', '*', '/', '(', ')', 'Clean all', 'Clean last', '=']
    };
  },
  methods: {
    handleClick(value) {
      switch(value) {
        case '=':
          this.$emit('execution');
          break;
        case 'Clean all':
          console.log('clean all');
          this.$emit('cleaningAll');
          break;
        case 'Clean last':
          console.log('clean last')
          this.$emit('cleaningLast');
          break;
        default:
          this.$emit('symbolAdding', value);
          break;
      }
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
.keyboard__btn:nth-child(17) {
  width: 156px;
  margin: 0 8px 8px 0;
}
.keyboard__btn:nth-child(18) {
  width: 156px;
  margin: 0 0 8px 0;
}
.keyboard__btn:last-child {
  width: 100%;
  margin: 0;
}
</style>
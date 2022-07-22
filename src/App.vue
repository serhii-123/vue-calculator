<template>
  <text-block
      class="app__text-block"
      :text="text"
  ></text-block>
  <keyboard
    @symbolAdding="addSymbol"
    @cleaningAll="cleanAll"
    @cleaningLast="cleanLast"
    @execution="executeExpression"
  ></keyboard>
</template>

<script>
import TextBlock from '@/components/textBlock'
import Keyboard from '@/components/keyboard'

export default {
  components: {
    TextBlock,
    Keyboard
  },
  data() {
    return {
      text: ''
    };
  },
  methods: {
    addSymbol(value) {
      this.text += value;
    },
    cleanAll() {
      console.log('cock');
      this.text = '';
    },
    cleanLast() {
      this.text = this.text.slice(0, -1);
    },
    executeExpression() {
      try {
        let result = eval(this.text).toString();
        this.text = result;
      } catch {
        console.log('Error!');
      }
    }
  }
}
</script>

<style>
#app {
  width: 320px;
}
.app__text-block {
  height: 74px;
  margin-bottom: 8px;
}
</style>
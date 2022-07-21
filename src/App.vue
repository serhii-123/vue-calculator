<template>
  <text-block
      class="app__text-block"
      :text="enteredValue"
  ></text-block>
  <keyboard></keyboard>
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
      enteredValue: ''
    };
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
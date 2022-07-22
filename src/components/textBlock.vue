<template>
  <div class="text-block">
    <p class="text-block__text">{{text}}</p>
  </div>
</template>

<script>
export default {
  name: "text-block",
  props: {
    text: [String, Number]
  }
}
</script>

<style scoped>
.text-block {
  display: flex;
  justify-content: left;
  align-items: center;
  padding: 10px;
  background-color: rgb(50, 50, 50);
}
.text-block__text {
  overflow: hidden;
  font-family: sans-serif;
  font-size: 20px;
  color: rgb(255, 255, 255);
}
</style>
<template>
  <div class="text-block">
    <p class="text-block__text">{{text}}</p>
  </div>
</template>

<script>
export default {
  name: "text-block",
  props: {
    text: String
  }
}
</script>

<style scoped>
.text-block {
  padding: 20px;
  background-color: rgb(50, 50, 50);
}
.text-block__text {
  text-overflow: ellipsis;
  font-family: sans-serif;
  font-size: 20px;
}
</style>
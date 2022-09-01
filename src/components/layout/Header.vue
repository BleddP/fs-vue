<template>
  <div class="header">
    <h1>{{ title }}</h1>
  </div>
</template>

<script>
export default {
  name: "Header",
  props: {
    title: String,
  },
};
</script>

<style>
.header {
  background-color: rgb(192, 192, 192);
  padding: 24px;
}
</style>
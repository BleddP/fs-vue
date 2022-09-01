<template>
  <div>
    <h1>Hello Component</h1>
    <h4>{{ title }}</h4>
  </div>
</template>

<script>
export default {
  name: "Hello",
  props: {
    title: String,
  },
};
</script>
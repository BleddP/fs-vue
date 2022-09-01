<template>
  <li>
    <h4>{{ task.title }}</h4>
  </li>
</template>

<script>
export default {
  name: "TaskItem",
  props: {
    task: Object,
  },
};
</script>

<style>
</style>
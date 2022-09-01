<template>
  <div>
    <input type="text" @input="handleInputChange" />
    <button class="primary" @click="filterTheList">{{ buttonText }}</button>
  </div>
</template>

<script>
export default {
  name: "TaskFilter",
  props: {
    buttonText: String
  },
  data() {
    return {
        input: '',
    }
  },
  methods: {
    handleInputChange(e) {
        this.input = e.target.value
    },
    filterTheList() {
        this.$emit("applyFilter", this.input)
    }
  }
};
</script>

<style>
</style>
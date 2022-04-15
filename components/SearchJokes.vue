<template>
  <form @submit.prevent="onSubmit">
    <input type="text" class="text" v-model="text" placeholder="Search Jokes...">
    <input type="submit" class="btn" value="Search Jokes">
  </form>
</template>

<script>
export default {
  name: "SearchJokes",
  data() {
    return {
      text: ""
    };
  },
  methods: {
    onSubmit() {
      this.$emit("search-text", this.text);
      this.text = "";
    }
  }
};
</script>

<style>
.btn {
  display: inline-block;
  background: #333;
  color: #fff;
  padding: 0.3rem 1rem;
  margin-right: 0.5rem;
}
.text {
  display: inline-block;
  padding: 0.3rem 1rem;
  margin-right: 0.5rem;
  border: 2px solid #333
}
</style>

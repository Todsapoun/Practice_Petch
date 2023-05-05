<template>
  <div>
    <h1 v-bind:style="colors">{{ text }}</h1>
    <button @click="changeColor">Change Color</button>

    <br /><br />

    <button
      v-bind:class="{ green: boolean, blue: !boolean }"
      @click="boolean = !boolean"
    ></button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      text: "test",
      colors: { color: "blue" },
      boolean: true,
    };
  },
  methods: {
    changeColor() {
      this.colors.color = "red";
    },
  },
};
</script>

<style scoped>
.green {
  background-color: green;
  width: 100px;
  height: 100px;
}
.blue {
  background-color: blue;
  width: 100px;
  height: 100px;
}
</style>
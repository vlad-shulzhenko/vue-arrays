<template>
  <ArrayList :array-list="resultArray" />
</template>

<script lang="ts">
import { defineComponent } from "vue";
import array from "@/api/array.json";
import ArrayList from "@/components/ArrayList.vue";

export default defineComponent({
  name: "App",
  components: {
    ArrayList,
  },

  setup() {
    return { resultArray: array };
  },
});
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>

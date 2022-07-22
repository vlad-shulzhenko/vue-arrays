<template>
  <div class="ArrayItem" :style="indent">
    <span>id: {{ arrayItem.id }}</span>
    <span>name: {{ arrayItem.name }}</span>
  </div>
  <ArrayItem
    v-for="item of arrayItem.children"
    :array-item="item"
    :key="item"
    :depth="depth + 1"
  />
</template>

<script>
import { defineComponent } from "vue";
export default defineComponent({
  props: ["arrayItem", "depth"],
  computed: {
    indent() {
      return { transform: `translateX(${this.depth * 20}px)` };
    },
  },
});
</script>

<style>
.ArrayItem {
  width: 300px;
  display: flex;
  grid-gap: 50px;
  border: 1px solid black;
  padding: 5px 10px;
  margin-bottom: 10px;
  border-radius: 12px;
}
</style>

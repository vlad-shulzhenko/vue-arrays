<template>
  <h1>Array List</h1>
  <div class="array-list">
    <ArrayItem
      v-for="item of arrayList"
      :key="`${Math.random()}` + item.id"
      :array-item="item"
      :depth="0"
    />
  </div>
</template>

<script>
import { defineComponent } from "vue";
import ArrayItem from "@/components/ArrayItem";

export default defineComponent({
  props: ["arrayList", "depth"],
  components: { ArrayItem },
});
</script>

<style>
.array-list {
  display: flex;
  width: 100%;
  flex-direction: column;
}
</style>

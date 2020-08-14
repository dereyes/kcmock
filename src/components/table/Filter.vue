<template>
  <div class="tableFilters input-group">
    <input type="text" placeholder="Search">
    <div class="input-group-button">
      <button class="hollow button" href="#" @click="overlay = !overlay">Filters</button>
    </div>
    <ModalFilter/>
  </div>
</template>

<script>
//import ModalFilter from "./../../modal/Filters.vue";
import ModalFilter from "@/components/modal/test.vue";
export default {
  name: "TableFilter",
  components: {
    ModalFilter
  },
  data: () => ({
    overlay: false
  })
};
</script>

<style lang="scss" scoped>
input {
  margin-bottom: 0;
}
</style>

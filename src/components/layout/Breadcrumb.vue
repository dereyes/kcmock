<template>
  <a class="breadcrumb" href="#" @click="showPage(page)">{{text}}</a>
</template>

<script>
export default {
  name: "Breadcrumb",
  methods: {
    showPage(pageSelect) {
      this.$emit("changePage", pageSelect);
    }
  },
  props: ["page", "text"]
};
</script>

<style lang="scss" scoped>
.breadcrumb {
  &::before {
    font-family: "Font Awesome 5 Free";
    font-weight: 900;
    content: "\f104 ";
  }
}
</style>
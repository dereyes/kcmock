<template>
  <div id="window">
    <v-main id="page">
      <router-view></router-view>
    </v-main>
    <Nav/>
  </div>
</template>

<script>
import Nav from "@/components/layout/Nav";

export default {
  name: "layout",
  components: {
    Nav
  },
  props: {
    header: {
      required: false,
      default: null
    },
    footer: {
      required: false,
      default: null
    }
  }
};
</script>

<style lang="scss" scoped>
#window {
  display: flex;
  flex-direction: column;
  height: 100vh;
  width: 100vw;
}
#page {
  flex: 1 1;
  padding: 1rem;
}
</style>


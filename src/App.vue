<template>
  <div id="app" class="app">
    <v-app id="inspire">
      <router-view></router-view>
    </v-app>
  </div>
</template>

<script>
export default {
  name: "App"
};
</script>

<style lang="scss" scoped>
html,
body,
#app,
#inspire,
.v-application--wrap {
  height: 100vh;
  width: 100vw;
}
</style>

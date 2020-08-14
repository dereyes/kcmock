<template>
  <v-bottom-navigation v-model="bottomNav" dark app>
    <v-btn :to="{ name: 'home' }">
      <!-- <span>Home</span> -->
      <v-icon>mdi-home</v-icon>
    </v-btn>

    <v-btn :to="{ name: 'page-library' }">
      <!-- <span>Library</span> -->
      <v-icon>mdi-library</v-icon>
    </v-btn>

    <v-btn>
      <!-- <span>Notifications</span> -->
      <v-icon>mdi-bell</v-icon>
    </v-btn>

    <v-btn>
      <!-- <span>Settings</span> -->
      <v-icon>mdi-cog</v-icon>
    </v-btn>
  </v-bottom-navigation>
  <!-- <div id="nav" class="expanded button-group">
    <a class="button" @click="showPage('home')">
      <i class="fas fa-home fa-2x"></i>
    </a>
    <a class="button" @click="showPage('library')">
      <i class="fas fa-book-open fa-2x"></i>
    </a>
    <a class="button" @click="showPage('notifications')">
      <i class="fas fa-bell fa-2x"></i>
    </a>
  </div>-->
</template>

<script>
export default {
  name: "Nav",
  // methods: {
  //   showPage(pageSelect) {
  //     this.$emit("changePage", pageSelect);
  //   }
  // }
  data() {
    return {
      bottomNav: 0
    };
  }
  // computed: {
  //   color() {
  //     switch (this.bottomNav) {
  //       case 0:
  //         return "blue-grey";
  //       case 1:
  //         return "teal";
  //       case 2:
  //         return "brown";
  //       case 3:
  //         return "indigo";
  //     }
  //   }
  // }
};
</script>
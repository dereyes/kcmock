<template>
  <div>
    <h1>Library</h1>
    <TableFilter/>
    <table>
      <thead>
        <tr>
          <th class="headerSort">Name</th>
        </tr>
      </thead>
      <tbody>
        <tr v-for="(rows, index) in rows" :key="`row-${index}`">
          <td>
            <a href="#" @click="showPage('songs')">{{rows}}</a>
          </td>
        </tr>
      </tbody>
    </table>
  </div>
</template>

<script>
import TableFilter from "./table/Filter";
export default {
  name: "Library",
  data: function() {
    return {
      rows: [
        "All Songs",
        "Anime Openings",
        "Anime Openings",
        "Anime Openings",
        "Anime Openings",
        "Anime Openings"
      ]
    };
  },
  components: {
    TableFilter
  },
  methods: {
    showPage(pageSelect) {
      this.$emit("changePage", pageSelect);
    }
  }
};
</script>

<style lang="scss" scoped>
th.headerSort::after {
  font-family: "Font Awesome 5 Free";
  font-weight: 900;
  content: " \f15d";
}
td a {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  &::after {
    font-family: "Font Awesome 5 Free";
    font-weight: 900;
    content: "\f0da";
  }
}
</style>
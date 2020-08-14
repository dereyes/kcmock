<template>
  <div>
    <Breadcrumb text="Library" page="library" @changePage="showPage($event)"/>
    <h1>Anime Openings</h1>
    <TableFilter/>
    <table>
      <thead>
        <tr>
          <th class="headerSort">Name</th>
          <th>Artist</th>
        </tr>
      </thead>
      <tbody>
        <tr v-for="(row, index) in rows" :key="`row-${index}`">
          <td colspan="2">
            <div class="rowWrapper">
              <a class="rowMain" href="#">
                {{row.name}}
                <br>
                <small>{{row.artist}}</small>
              </a>
              <a href="#">
                <i class="fas fa-ellipsis-v"></i>
              </a>
            </div>
          </td>
        </tr>
      </tbody>
    </table>
  </div>
</template>

<script>
import Breadcrumb from "../layout/Breadcrumb";
import TableFilter from "./table/Filter";
export default {
  name: "Library",
  data: function() {
    return {
      rows: [
        {
          name: "A Cruel Angel's Thesis",
          artist: "Yoko Takahashi"
        },
        {
          name: "All Star",
          artist: "Smash Mouth"
        },
        {
          name: "Tank!",
          artist: "The Seatbelts"
        }
      ]
    };
  },
  components: {
    Breadcrumb,
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
.rowWrapper {
  align-items: center;
  display: flex;
  flex: 1 1;
  flex-direction: row;

  .rowMain {
    flex: 1 1;
  }
}
</style>
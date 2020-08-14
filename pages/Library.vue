<template>
  <div>
    <h3 class="text-h3">My Library</h3>
    <TableFilter/>
  </div>
</template>

<script>
import TableFilter from "@/components/table/Filter";
export default {
  components: {
    TableFilter
  },
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
  name: "page-library"
};
</script>

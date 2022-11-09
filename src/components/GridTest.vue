<template>
  <div class="grid">
    <vue-good-table
      :columns="columns"
      :rows="rows"
      :search-options="{
        enabled: true,
      }"
    />
  </div>
</template>
<script>
import "vue-good-table/dist/vue-good-table.css";
import { VueGoodTable } from "vue-good-table";
export default {
  components: { VueGoodTable },
  data() {
    return {
      columns: [
        {
          label: "Name",
          field: "name",
        },
        {
          label: "Age",
          field: "age",
          type: "number",
        },
        {
          label: "Created On",
          field: "createdAt",
          type: "date",
          dateInputFormat: "yyyy-MM-dd",
          dateOutputFormat: "MMMM do yyyy",
        },
      ],
      rows: [
        { id: 1, name: "John", age: 20, createdAt: "2019-05-05" },
        { id: 2, name: "Jane", age: 24, createdAt: "2021-10-25" },
        { id: 3, name: "Susan", age: 16, createdAt: "2016-10-30" },
        { id: 4, name: "Chris", age: 55, createdAt: "2018-09-11" },
        { id: 5, name: "Dan", age: 40, createdAt: "2011-10-21" },
        { id: 6, name: "Max", age: 33, createdAt: "2012-12-31" },
      ],
    };
  },
};
</script>
<style scoped>
.grid {
  margin-left: 88px;
  margin-right: 88px;
  margin-top: 30px;
}
</style>

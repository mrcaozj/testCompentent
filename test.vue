<template>
  <el-table-column :prop="prop" :label="label" sortable :width="width">
    <template slot-scope="scope">
      <columnsComponentRender
        :index="index"
        :prop="prop"
        :row="scope.row"
        :value="scope.row[prop]"
        :columnsRender="columnsRender"
        :rendertype="rendertype"
        :ownmethod="ownmethod"
      ></columnsComponentRender>
    </template>
  </el-table-column>
</template>

<script>
import columnsComponentRender from "./columnsComponentRender";
export default {
  name: "ColumnsComponent",
  created() {},
  props: ["prop", "label", "index", "width", "columnsRender","rendertype","ownmethod"],
  mounted() {},
  components: { columnsComponentRender },
  data() {
    return {};
  },
  methods:{
    gogo(){
      alert(1)
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>

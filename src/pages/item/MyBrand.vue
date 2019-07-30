<template>
  <div>
    <v-data-table
      :headers="headers"
      :items="brands"
      :pagination.sync="pagination"
      :total-items="totalBrands"
      :loading="loading"
      class="elevation-1"
    >
      <template slot="items" slot-scope="props">
        <td class="text-xs-center">{{ props.item.id }}</td>
        <td class="text-xs-center">{{ props.item.name }}</td>
        <td class="text-xs-center"><img v-if="props.item.image" :src="props.item.image" width="130" height="40"/></td>
        <td class="text-xs-center">{{ props.item.letter }}</td>
      </template>
    </v-data-table>
  </div>
</template>

<script>
  export default {
    name: "myBrand"
  }
</script>

<!-- scoped:当前样式只作用于当前组件的节点 -->
<style scoped>

</style>

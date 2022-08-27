<template>
  <div id="app">
    <ActionButton
      @add-entry="addEntryToTable"
    />
    <TableComponent
      ref="tableComponent"
    />
  </div>
</template>

<script>
  import TableComponent from '@/components/TableComponent'
  import ActionButton from '@/components/ActionButton'

  export default {
    components: {
      TableComponent,
      ActionButton
    },
    methods: {
      addEntryToTable(entry) {
        this.$refs?.tableComponent.tableData.push(entry)
      }
    }
  }
</script>

<style lang="scss">
  * {
    box-sizing: border-box;
    font-family: "helvetica";
  }
</style>
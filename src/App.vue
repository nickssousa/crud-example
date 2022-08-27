<template>
  <div id="app">
    <TableComponent />
  </div>
</template>

<script>
  import TableComponent from '@/components/TableComponent'

  export default {
    components: {
      TableComponent
    }
  }
</script>

<style lang="scss">
  * {
    box-sizing: border-box;
    font-family: "helvetica";
  }
</style>
<template>
  <div
    class="table-component"
  >
    <div
      class="table-header"
    >
      <div
        class="table-row"
      >
        <div
          v-for="(label, idx) in headerLabels"
          :key="`table_header_label_${ idx }`"
          class="table-column"
        >
          {{ label }}
        </div>
      </div>
    </div>

    <div
      class="table-body"
    >
      <div
        v-for="(row, idx) in tableData"
        :key="`table_body_row_${ idx }`"
        class="table-row"
      >
        <div
          v-for="(item, idx) in row"
          :key="`table_body_item_${ idx }`"
          class="table-column"
        >
          {{ item }}
        </div>
      </div>
    </div>
  </div>
</template>

<script>
  export default {
    data() {
      return {
        headerLabels: ['Código', 'Data', 'Nome', 'Quantidade', 'Valor'],
        tableData: [
          [123, '27/08/2022', 'Águas Teresina', 100, 'R$ 1,50'],
          [456, '22/05/2022', 'Eletrobrás', 300, 'R$ 2,50'],
          [789, '23/08/2021', 'G3', 150, 'R$ 13,50']
        ]
      }
    }
  }
</script>

<style lang="scss" scoped>
  .table-component {
    width: fit-content;
    border-top: 1px solid #888;
    border-left: 1px solid #888;
    font-size: 12px;

    .table-header {
      background-color: #ddd;
    }

    .table-row {
      display: flex;
      min-width: 600px;
    }

    .table-column {
      flex: 1;
      padding: 4px 10px;
      border-right: 1px solid #888;
      border-bottom: 1px solid #888;
    }
  }
</style>
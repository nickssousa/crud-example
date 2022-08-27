<template>
  <div
    class="action-button"
  >
    <button
      @click="submit"
    >
      adicionar item
    </button>
  </div>
</template>

<script>
  export default {
    data() {
      return {
        entry: [101, '01/02/2022', 'Cepisa', 12, 'R$ 2,00']
      }
    },
    methods: {
      submit() {
        this.$emit('add-entry', this.entry)
      }
    }
  }
</script>

<style lang="scss" scoped>
  .action-button {
    margin-bottom: 10px;
    cursor: pointer;
  }
</style>
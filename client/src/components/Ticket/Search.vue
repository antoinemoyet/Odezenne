<template>
    <form class="search-form">
      <div class="search-input">
        <input type="text" v-model="search" placeholder="Recherchez une ville" required @keyup="emitSearch"/>
        <img src="../../assets/images/trait_2.svg">
      </div>
    </form>
</template>

<script>
  export default {
    name: 'search',
    data() {
      return {
        search: '',
      };
    },
    methods: {
      emitSearch() {
        this.$parent.$emit('emitSearch', this.search);
      },
    },
  };
</script>

<style lang="scss">
  .search-form{
    width: 100%;
    .search-input{
      width: 30%;
      margin: 0 auto;
      input{
        width: 100%;
        height: 50px;
        background-color: transparent;
        border: none;
        outline: none;
        font-family: "Roboto Condensed";
        font-size: 1rem;
        font-weight: 700;
        position: relative;
        text-align: center;
      }
    }
  }
</style>

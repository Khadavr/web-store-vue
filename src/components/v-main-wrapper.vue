<template>
    <div class="v-main-wrapper">
      <p>{{title}}</p>
      <v-catalog />
      <v-cart/>
    </div>
</template>

<script>
  import VCatalog from './v-catalog'
  import VCart from './v-cart'
  export default {
    name: 'v-main-wrapper',
    components: {VCatalog, VCart},
    props: {},
    data() {
        return {
            title: 'Main wrapper'
        }
    },
    computed: {},
    methods: {},
    watch: {},
    mounted() {
        console.log('I am working!');
    }
  }
</script>

<style>
  .v-main-wrapper {
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      max-width: 900px;
      margin: 0 auto;
  }

</style>

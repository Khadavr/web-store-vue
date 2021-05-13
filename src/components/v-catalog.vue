<template>
    <div class="v-catalog">
        <h2>Catalog</h2>
        <v-catalog-item />
    </div>
</template>
<script>
import VCatalogItem from './v-catalog-item.vue'
export default {
    name: 'v-catalog',
    components: {
        VCatalogItem
    },
    props: {},
    data() {
        return {}
    },
    computed: {}
}
</script>
<style>
    
</style>
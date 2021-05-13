<template>
    <div class="v-catalog">
        <h2>Catalog</h2>
        <div class="v-catalog_list">
          <v-catalog-item
            v-for="product in products"
            :key="product.article"
            v-bind:product_data="product"
            @sendArticle="showData"
          />
         </div>
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
        return {
  products: [
    {
      image: "1.jpg",
      name: "T-shirt 1",
      price: 2100.234234234,
      article: "T1",
      available: true,
      category: "Мужские"
    },
    {
      image: "2.jpg",
      name: "T-shirt 2",
      price: 3150.12312412,
      article: "T2",
      available: true,
      category: "Унисекс"
    },
    {
      image: "3.jpg",
      name: "T-shirt 3",
      price: 4200.51524,
      article: "T3",
      available: false,
      category: "Мужские"
    },
    {
      image: "4.jpg",
      name: "T-shirt 4",
      price: 5300.1245512,
      article: "T4",
      available: true,
      category: "Мужские"
    },
    {
      image: "5.jpeg",
      name: "T-shirt 5",
      price: 6500.3522314,
      article: "T5",
      available: false,
      category: "Унисекс"
    },
    {
      image: "6.jpg",
      name: "T-shirt 6",
      price: 8700.4124123,
      article: "T6",
      available: true,
      category: "Унисекс"
    }
  ]
        }
    },
    computed: {},
    methods: {
        showData(data) {
          console.log(data)
        }
    }
}
</script>
<style lang="scss">
    .v-catalog {
        &_list {
           display: flex;
           flex-wrap: wrap;
           justify-content: space-between;
           align-items: center;
        }
    }    
</style>
    

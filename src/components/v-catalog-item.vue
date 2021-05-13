<template>
    <div class="v-catalog-item">
        <img class="v-catalog-item_image" :src=" require('../assets/images/' + product_data.image) " alt="img" /> 
        <p class="catalog-item-name">{{product_data.name}}</p>
        <p class="catalog-item-price">Price: {{product_data.price}} $</p>
        <button class="catalog-item_add_btn btn" 
                @click="sendDataToParent">
                Add to cart
        </button>
    </div>
</template>
<script>
export default {
    name: 'v-catalog-item',
    props: {
        product_data: {
          type: Object,
          default() {
              return {}
          }
        }
    },
    data() {
        return {}
    },
    computed: {},
    methods: {
        sendDataToParent() {
            this.$emit('sendArticle', this.product_data.article)
        }
    }
}
</script>
<style lang="scss">
   .v-catalog-item {
       flex-basis: 25%;
       box-shadow: 0 0 8px 0 #e0e0e0;
       padding: $padding*2;
       margin-bottom: $margin*2;
       &_image {
           width: 150px;
       }
   } 
</style>
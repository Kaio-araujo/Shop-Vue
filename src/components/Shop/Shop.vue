<template>
    <shop-products-list :products="products" class="p-3"></shop-products-list>
</template>

<script>
    import ShopProductsList from './ShopProductsList';
    import { eventBus } from '../../main';

    export default {
        name: "shop",
        components : {
            ShopProductsList,
        },
        data() {
            return {
                products: []
            }
        },
        created() {
            this.products = eventBus.products;
            eventBus.$on('ipdate:products', (products) => {
                this.products = products;
            })
        },
    }
</script>

<style scoped>

</style>
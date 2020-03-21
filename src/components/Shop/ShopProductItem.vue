<template>
    <div class="w-25 p-3 product-container d-flex flex-column">
        <div class="d-flex flex-row justify-content-center">
            <img :src="product.img" style="height: 150px">
        </div>
        <div>
            <h3>{{ product.title }}</h3>
            <hr>
        </div>
        <div>
            <p>{{ product.description }}</p>
        </div>
        <div>
            <span>{{ product.price }} €</span>
            <button class="btn btn-primary btn-sm float-right" @click="addProductToCart()">Commander</button>
        </div>
    </div>
</template>

<script>
    import { eventBus } from '../../main'
    export default {
        name: "ShopProductItem",
        props: ['product'],
        methods: {
            addProductToCart() {
                eventBus.addProductToCart( {...this.product} )
            }
        }
    }
</script>

<style scoped>

.product-container {
    height: 400px;
}

p {
    font-size: 12px;
    overflow: scroll;
    max-height: 70px;
}

</style>
<template>
<div>
    <cart-products-list :cart="cart" class="p-3"></cart-products-list>
</div>
</template>

<script>
    import CartProductsList from './CartProductsList';
    import { eventBus } from '../../main';

    export default {
        name: "cart",
        components : {
            CartProductsList,
        },
        data() {
            return {
                cart: []
            }
        },
        created() {
            this.cart = eventBus.cart;
            eventBus.$on('update:cart', (cart) => {
                this.cart = cart;
            })
        },
    }
</script>

<style scoped>

</style>
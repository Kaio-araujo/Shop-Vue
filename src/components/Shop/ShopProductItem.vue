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
            <span>{{ product.price }}</span>
            <button class="btn btn-primary btn-sm float-right">Commander</button>
        </div>
    </div>
</template>

<script>
    export default {
        name: "ShopProductItem",
        data() {
            return {
                product: {
                    img: 'https://store.storeimages.cdn-apple.com/4668/as-images.apple.com/is/MBP13ST-201807?wid=324&hei=324&fmt=jpeg&qlt=95&op_usm=0.5,0.5&.v=1531249597131',
                    title: 'Macbook Pro',
                    description: 'Avec le MacBook Pro, l’ordinateur portable atteint des sommets inédits en matière de performances et de portabilité. Grâce à des processeurs et une mémoire hautes performances, à des graphismes avancés et à un système de stockage d’une rapidité fulgurante, il donne vie à toutes vos idées plus vite que jamais. Et comme il pèse moins de 1,4 kg, il vous accompagne partout, quelles que soient les contrées où vous mène votre imagination.',
                    price: '1 499,00 € ',
                }
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
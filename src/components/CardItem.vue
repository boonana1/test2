<template>
    <div class="card" v-for="(product, i) in products" :key="i">
        <div class="card__badge"><img :src="require(`@/assets/img/icon-ruble.svg`)" alt="">{{ product.badge }}</div>
        <img :src="require(`@/assets/img/${product.img}`)" alt="Изображение товара" class="card__img">
        <div class="card__info">
            <h3 class="card__price">{{ product.price }}</h3>
            <span class="card__name">{{ product.name }}</span>
        </div>
        <button class="card__buyButton">Купить</button>
    </div>
</template>

<script>
export default {
    name: "CardItem",
    props: {
        products: Array
    }
}
</script>

<style scoped>
.card {
    gap: 12px;
    flex: 1 0 0;
    grid-row: span 3;
    display: grid;
    grid-template-rows: subgrid;
    overflow: hidden;
}

.card .card__badge {
    display: inline-flex;
    padding: 2px 4px;
    align-items: center;
    gap: 3px;
    border-radius: 100px;
    background: linear-gradient(145deg, #5856D6 4.04%, #D000A2 100%), linear-gradient(145deg, #5856D6 4.04%, #AF52DE 100%);
    color: #fff;
    position: absolute;
    text-align: center;
    font-size: 10px;
    font-style: normal;
    font-weight: 600;
    line-height: 13px;
    letter-spacing: 0.066px;
}

.card img.card__img {
    max-width: 100%;
}

.card .card__info {
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    gap: 4px;
    max-width: 100%;
}

.card .card__price {
    color: var(--label-colors-primary, #000);
    font-size: 14px;
    font-style: normal;
    font-weight: 600;
    line-height: 18px;
    letter-spacing: -0.154px;
}

.card .card__name {
    color: #000;
    font-size: 12px;
    font-style: normal;
    font-weight: 400;
    line-height: 16px;
    text-align: left;
    overflow: hidden;
    display: -webkit-box;
    -webkit-box-orient: vertical;
    -webkit-line-clamp: 2;
    white-space: pre-wrap;
}

.card .card__buyButton {
    display: flex;
    padding: 8px 24px;
    justify-content: center;
    align-items: center;
    align-self: stretch;
    border-radius: 12px;
    background: #5856D6;
    color: #fff;
    appearance: none;
    border: none;
    text-align: center;
    font-size: 14px;
    font-style: normal;
    font-weight: 600;
    line-height: 18px;
    letter-spacing: -0.154px;
}
</style>
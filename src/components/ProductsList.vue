<template>
    <div class="products">
        <card-item :products="products" />
    </div>
</template>
  
<script>
import CardItem from './CardItem.vue';
export default {
    components: { CardItem },
    name: 'ProductsList',
    data() {
        return {
            products: [
                { badge: "1 120", img: "4a7512d5c8a576c5b43437e68453e80b.png", price: "112 000 ₽", name: 'Apple MacBook Air 13.6" (M2 8C CPU/8C GPU, 8 Gb, 256 Gb SSD) Темно-синий (MLY33)' },
                { badge: "1 120", img: "7626ec4457a85a565322cbfc44205be9.png", price: "119 000 ₽", name: 'Apple iPhone 14 Pro Max 256 gb Deep Purple' },
                { badge: "1 120", img: "4a7512d5c8a576c5b43437e68453e80b.png", price: "112 000 ₽", name: 'Apple MacBook Air 13.6" (M2 8C CPU/8C GPU, 8 Gb, 256 Gb SSD) Темно-синий (MLY33)' },
                { badge: "1 120", img: "7626ec4457a85a565322cbfc44205be9.png", price: "119 000 ₽", name: 'Apple iPhone 14 Pro Max 256 gb Deep Purple' },
                { badge: "1 120", img: "4a7512d5c8a576c5b43437e68453e80b.png", price: "112 000 ₽", name: 'Apple MacBook Air 13.6" (M2 8C CPU/8C GPU, 8 Gb, 256 Gb SSD) Темно-синий (MLY33)' },
                { badge: "1 120", img: "7626ec4457a85a565322cbfc44205be9.png", price: "119 000 ₽", name: 'Apple iPhone 14 Pro Max 256 gb Deep Purple' },
                { badge: "1 120", img: "4a7512d5c8a576c5b43437e68453e80b.png", price: "112 000 ₽", name: 'Apple MacBook Air 13.6" (M2 8C CPU/8C GPU, 8 Gb, 256 Gb SSD) Темно-синий (MLY33)' },
                { badge: "1 120", img: "7626ec4457a85a565322cbfc44205be9.png", price: "119 000 ₽", name: 'Apple iPhone 14 Pro Max 256 gb Deep Purple' },
                { badge: "1 120", img: "4a7512d5c8a576c5b43437e68453e80b.png", price: "112 000 ₽", name: 'Apple MacBook Air 13.6" (M2 8C CPU/8C GPU, 8 Gb, 256 Gb SSD) Темно-синий (MLY33)' },
                { badge: "1 120", img: "7626ec4457a85a565322cbfc44205be9.png", price: "119 000 ₽", name: 'Apple iPhone 14 Pro Max 256 gb Deep Purple' },
                { badge: "1 120", img: "4a7512d5c8a576c5b43437e68453e80b.png", price: "112 000 ₽", name: 'Apple MacBook Air 13.6" (M2 8C CPU/8C GPU, 8 Gb, 256 Gb SSD) Темно-синий (MLY33)' },
                { badge: "1 120", img: "7626ec4457a85a565322cbfc44205be9.png", price: "119 000 ₽", name: 'Apple iPhone 14 Pro Max 256 gb Deep Purple' },
            ]
        }
    }
}
</script>
<style scoped>
h3 {
    margin: 40px 0 0;
}

ul {
    list-style-type: none;
    padding: 0;
}

li {
    display: inline-block;
    margin: 0 10px;
}

button {
    appearance: none;
    border: none;
}

.products {
    display: grid;
    grid-auto-flow: dense;
    grid-template-columns: repeat(auto-fit, minmax(min(100%, 160px), 1fr));
    grid-auto-rows: auto;
    container-type: inline-size;
    margin-top: 24px;
    padding-bottom: 16px;
    column-gap: 16px;
    row-gap: 32px;
}
</style>
  
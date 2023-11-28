<template>
  <IndexBar :index-list="categories">
    <section v-for="category in categories" :key="category">
      <IndexAnchor :index="category">
        {{ category }}
      </IndexAnchor>

      <ul
        v-for="num in 4"
        :key="`${category}-${num}`"
      >
        <ProductCard :category="category" :item="item" />
      </ul>
    </section>
  </IndexBar>
</template>

<script>
import { IndexBar, IndexAnchor } from 'vant'
import ProductCard from './ProductCard'

export default {
  name: 'ScrollMenu',
  components: {
    IndexBar,
    IndexAnchor,
    ProductCard
  },

  data() {
    return {
      categories: [
        'Populair ❤',
        'Menus & Chicken Mix',
        'The BOX',
        'Voorgerechten',
        'Pan pizza medium',
        'Classic pizza medium',
        'Pan pizza large',
        'Classic pizza large',
        'Cheesy crust pizza large',
        'Desserten',
        'Dranken'
      ],

      item: {
        name: 'Pepperoni lovers pan pizza medium',
        details: 'Pepperoniworst, mozzarella, tomatensaus.',
        price: '$15.0'
      }
    }
  }
};
</script>

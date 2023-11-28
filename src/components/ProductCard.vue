<template>
  <li class="product-item">
    <article>
      <h2>{{ category }} -- {{ item.name }}</h2>
      <p>{{ item.details }}</p>
      <br>

      {{ item.price }}
    </article>

    <img src="https://picsum.photos/150/150">
  </li>
</template>

<script type="text/javascript">
  export default {
    name: 'ProductCard',
    props: {
      category: {
        type: String
      },

      item: {
        required: true
      }
    }
  };
</script>

<template>
  <div class="row">
    <Carousel/>
    <ProductList/>
    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Voluptate quisquam temporibus id excepturi culpa aperiam facere laudantium corporis? Accusamus ullam at eum ratione et consectetur ab labore suscipit iusto quaerat.</p>
  </div>
</template>

<script>
import Carousel from '../components/Carousel.vue'
import ProductList from '../components/ProductList.vue'

export default {
  name: 'Home',
  components: { ProductList, Carousel }
}
</script>

<template>
  <BasicLayouts>
    <h2>Nuestra Tienda</h2>
    <Cart />
  </BasicLayouts>
</template>

<script>
import BasicLayouts from '../layouts/BasicLayouts.vue';
import Cart from '../components/Cart.vue';
import { useRoute, useRouter } from 'vue-router';
export default {
  name: 'Store',
  components: {
    BasicLayouts,
    Cart
  },
};
</script>
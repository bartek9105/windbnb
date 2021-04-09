<template>
  <div class="apartments">
    <apartment-item
      :apartment="apartment"
      v-for="(apartment, index) in apartments"
      :key="index"
    />
  </div>
</template>

<script>
import ApartmentItem from '@/components/Apartments/ApartmentItem'

export default {
  name: 'ApartmentsList',
  props: {
    apartments: {
      type: Array,
      required: true
    }
  },
  components: {
    ApartmentItem
  }
}
</script>

<style lang="scss" scoped>
.apartments {
  max-width: 1248px;
  margin: 0 auto;
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  column-gap: 2rem;
  row-gap: 3.125rem;
}
</style>

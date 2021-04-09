<template>
  <div>
    <app-navbar />
    <app-search-full v-if="searchFull" />
    <apartments-list :apartments="apartments" />
  </div>
</template>

<script>
import AppNavbar from '@/components/AppNavbar'
import AppSearchFull from '@/components/AppSearchFull'
import ApartmentsList from '@/components/Apartments/ApartmentsList'
import stays from '@/_data/stays.json'

export default {
  name: 'Home',
  components: {
    AppNavbar,
    AppSearchFull,
    ApartmentsList
  },
  data() {
    return {
      apartments: stays,
      searchFull: true
    }
  }
}
</script>

<style></style>

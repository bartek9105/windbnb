<template>
  <div>
    <app-navbar />
    <apartments-list :apartments="apartments" />
  </div>
</template>

<script>
import AppNavbar from '@/components/AppNavbar'
import ApartmentsList from '@/components/Apartments/ApartmentsList'
import stays from '@/_data/stays.json'

export default {
  name: 'Home',
  components: {
    AppNavbar,
    ApartmentsList
  },
  data() {
    return {
      apartments: stays
    }
  }
}
</script>

<style></style>

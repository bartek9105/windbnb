<template>
  <div class="navbar">
    <app-logo />
    <div class="searchbar"></div>
  </div>
</template>

<script>
import AppLogo from '@/components/AppLogo'

export default {
  name: 'AppNavbar',
  components: {
    AppLogo
  }
}
</script>

<style lang="scss" scoped>
.navbar {
  max-width: 1248px;
  margin: 0 auto;
  padding-top: 2rem;
}
</style>

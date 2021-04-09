<template>
  <div class="navbar">
    <app-logo />
    <app-search-bar />
  </div>
</template>

<script>
import AppLogo from '@/components/AppLogo'
import AppSearchBar from '@/components/AppSearchBar'

export default {
  name: 'AppNavbar',
  components: {
    AppLogo,
    AppSearchBar
  }
}
</script>

<style lang="scss" scoped>
.navbar {
  display: flex;
  justify-content: space-between;
  align-items: center;
  max-width: 1248px;
  margin: 0 auto 3.75rem auto;
  padding-top: 2rem;
}
</style>

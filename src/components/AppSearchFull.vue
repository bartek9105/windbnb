<template>
  <div>
    <div class="overlay"></div>
    <div class="search-wrapper">
      <div class="search">
        <input type="text" />
        <search-button />
      </div>
    </div>
  </div>
</template>

<script>
import SearchButton from '@/components/SearchButton'

export default {
  name: 'AppSearchFull',
  components: {
    SearchButton
  }
}
</script>

<style lang="scss" scoped>
.overlay {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: rgba(0, 0, 0, 0.5);
}
.search-wrapper {
  background-color: #fff;
  width: 100%;
  position: fixed;
  top: 0;
  left: 0;
  z-index: 2;
}
.search {
  max-width: 1248px;
  margin: 0 auto;
  padding: 5.625rem 0;
}
</style>

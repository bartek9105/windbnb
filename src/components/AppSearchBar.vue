<template>
  <div class="searchbar">
    <div>Add location</div>
    <div>Add guests</div>
    <div>
      <search-icon size="1.5x" class="search-icon" />
    </div>
  </div>
</template>

<script>
import { SearchIcon } from 'vue-feather-icons'

export default {
  name: 'AppSearchBar',
  components: {
    SearchIcon
  }
}
</script>

<style lang="scss" scoped>
.searchbar {
  display: flex;
  align-items: center;
  max-width: 297px;
  border-radius: 1rem;
  box-shadow: 0px 1px 6px rgba(0, 0, 0, 0.1);
  div {
    padding: 1rem;
    border-right: 1px solid #f2f2f2;
    color: #bdbdbd;
    font-size: 14px;
  }
}
.search-icon {
  color: $red;
}
</style>

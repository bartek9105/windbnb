<template>
  <button type="submit" class="btn">
    <search-icon size="1x" class="search-icon"></search-icon>
    <span>Search</span>
  </button>
</template>

<script>
import { SearchIcon } from 'vue-feather-icons'

export default {
  name: 'SearchButton',
  components: {
    SearchIcon
  }
}
</script>

<style lang="scss" scoped>
.btn {
  display: flex;
  align-items: center;
  background-color: $red;
  color: #f2f2f2;
  font-size: 0.875rem;
  box-shadow: 0px 1px 6px rgba(0, 0, 0, 0.1);
  border: 0;
  border-radius: 16px;
  padding: 1rem 1.625rem;
  cursor: pointer;
}
.search-icon {
  margin-right: 0.625rem;
}
</style>

<template>
  <div>
    <div class="overlay"></div>
    <div class="search-wrapper">
      <div class="search">
        <form @submit.prevent class="search-form">
          <div class="search-form__input-container">
            <label for="location" class="search-form__input-label"
              >Location</label
            >
            <input
              type="text"
              placeholder="Add location"
              class="search-form__input"
            />
          </div>
          <div class="search-form__input-container">
            <label for="location" class="search-form__input-label"
              >Guests</label
            >
            <input
              type="text"
              placeholder="Add guests"
              class="search-form__input"
            />
          </div>
          <search-button />
        </form>
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
  display: flex;
  max-width: 1248px;
  margin: 0 auto;
  padding: 5.625rem 0;
}
.search-form {
  width: 100%;
  display: grid;
  grid-template-columns: 45% 45% 10%;
  box-shadow: 0px 1px 6px rgba(0, 0, 0, 0.1);
  border-radius: 1rem;
  &__input-container {
    display: flex;
    flex-direction: column;
    border-radius: 1rem;
    padding: 0.75rem 1.625rem;
  }
  &__input-label {
    text-transform: uppercase;
    color: #333;
    font-weight: 700;
    font-size: 0.625rem;
    margin-bottom: 0.25rem;
  }
  &__input {
    border: 0;
    &::placeholder {
      color: #bdbdbd;
      font-size: 0.875rem;
      font-weight: 400;
    }
  }
}
</style>

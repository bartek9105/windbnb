<template>
  <div class="apartment">
    <img
      :src="apartment.photo"
      alt="apartment-photo"
      class="apartment__image"
    />
    <div class="apartment__info">
      <div class="apartment__info-left">
        <div class="apartment__badge" v-if="apartment.superHost">
          Super Host
        </div>
        <div class="apartment__type">{{ apartment.type }}</div>
        <div class="apartment__beds" v-if="apartment.beds">
          {{ apartment.beds }} beds
        </div>
      </div>
      <div class="apartment__rating">
        <star-icon size="1x" class="apartment__rating-star"></star-icon>
        {{ apartment.rating }}
      </div>
    </div>
    <h2 class="apartment__title">{{ apartment.title }}</h2>
  </div>
</template>

<script>
import { StarIcon } from 'vue-feather-icons'

export default {
  name: 'ApartmentItem',
  props: {
    apartment: {
      type: Object,
      required: true
    }
  },
  components: {
    StarIcon
  }
}
</script>

<style lang="scss" scoped>
.apartment {
  max-width: 395px;
  &__image {
    object-fit: cover;
    width: 100%;
    max-height: 267px;
    border-radius: 1.5rem;
    margin-bottom: 1rem;
  }
  &__info {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-bottom: 0.75rem;
  }
  &__info-left {
    display: flex;
    align-items: center;
  }
  &__title {
    max-width: 100%;
    text-overflow: ellipsis;
    overflow: hidden;
    white-space: nowrap;
    font-size: 1rem;
    font-weight: 600;
    color: #333;
  }
  &__badge {
    font-size: 0.75rem;
    font-weight: 700;
    color: #4f4f4f;
    border: 1px solid #4f4f4f;
    border-radius: 0.75rem;
    padding: 0.375rem 0.625rem;
    margin-right: 0.625rem;
  }
  &__type {
    margin-right: 1rem;
  }
  &__type,
  &__beds {
    font-size: 0.875rem;
    font-weight: 500;
    color: #828282;
  }
  &__rating {
    display: flex;
    align-items: center;
    font-size: 0.875rem;
    font-weight: 500;
    color: #4f4f4f;
  }
  &__rating-star {
    color: $red;
    margin-right: 0.375rem;
  }
}
</style>

<template>
  <div class="gallery">
      <figure class="gallery__item">
        <img src="@/img/hotel-1.jpg" alt="" class="gallery__photo">
      </figure>
      <figure class="gallery__item">
        <img src="@/img/hotel-2.jpg" alt="" class="gallery__photo">
      </figure>
      <figure class="gallery__item">
        <img src="@/img/hotel-3.jpg" alt="" class="gallery__photo">
      </figure>
    </div>
</template>

<style lang="scss" scoped>
  .gallery {
  display: flex;
  &__photo {
    width: 100%;
    display: block;
  }
  }
</style>
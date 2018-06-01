<template>
  <div class="hotel-view">
    <PhotoGallery></PhotoGallery>
  </div>
</template>

<script>
import PhotoGallery from '@/components/Content/TheHotelView/PhotoGallery.vue';

export default {
  components: {
    PhotoGallery,
    
    }
}
</script>


<style lang="scss" scoped>
  .hotel-view {
    background-color: #fff;
    flex: 1; // flex 1 grows the remaining width next to sidebar
  }
</style>



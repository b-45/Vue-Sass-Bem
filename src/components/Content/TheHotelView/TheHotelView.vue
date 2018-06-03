<template>
  <div class="hotel-view">
    <PhotoGallery></PhotoGallery>
    <HotelOverview></HotelOverview>
    <HotelDetail></HotelDetail>
    

  </div>
</template>

<script>
import PhotoGallery from '@/components/Content/TheHotelView/PhotoGallery.vue'
import HotelOverview from '@/components/Content/TheHotelView/HotelOverview.vue'
import HotelDetail from '@/components/Content/TheHotelView/HotelDetail.vue';


export default {
  components: {
    PhotoGallery,
    HotelOverview,
    HotelDetail
    
    }
}
</script>


<style lang="scss" scoped>
  .hotel-view {
    background-color: #fff;
    flex: 1; // flex 1 grows the remaining width next to sidebar
  }
</style>



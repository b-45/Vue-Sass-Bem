<template>
  <div class="hotel-view">
    <PhotoGallery></PhotoGallery>
    <HotelOverview></HotelOverview>
    <HotelDetail></HotelDetail>
    <CallToAction></CallToAction>
  </div>
</template>

<script>
import PhotoGallery from '@/components/Content/TheHotelView/PhotoGallery.vue'
import HotelOverview from '@/components/Content/TheHotelView/HotelOverview.vue'
import HotelDetail from '@/components/Content/TheHotelView/HotelDetail.vue'
import CallToAction from '@/components/Content/TheHotelView/CallToAction.vue';

export default {
  components: {
    PhotoGallery,
    HotelOverview,
    HotelDetail,
    CallToAction
    }
}
</script>

<style lang="scss" scoped>
  .hotel-view {
    background-color: #fff;
    flex: 1; // flex 1 grows the remaining width next to sidebar
  }
</style>



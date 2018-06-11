<template>
  <div class="content"> 
    <TheSidebar></TheSidebar>
    <TheHotelView></TheHotelView>
  </div>
</template>

<script>
import TheSidebar from '@/components/Content/TheSidebar/TheSidebar.vue'
import TheHotelView from '@/components/Content/TheHotelView/TheHotelView.vue'


export default {
  components: {
    TheSidebar,
    TheHotelView
  }
  
}
</script>

<style lang="scss" scoped>
  .content{
    display: flex; // places side bar and content side by side. 
   
   @media only screen and (max-width: 56.75em) {
      flex-direction: column;
    }
  }


</style>


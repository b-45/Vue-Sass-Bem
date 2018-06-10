<template>
  <div class="container">
    <TheHeading></TheHeading>
    <TheContent></TheContent>
  </div>
</template>

<script>
import TheHeading from '@/components/TheHeading.vue'
import TheContent from '@/components/Content/TheContent.vue'

export default {
  components: {
    TheHeading,
    TheContent
  }
}
</script>

<style lang="scss" scoped>
.container {
  max-width: 120rem; // width for this container (1200px) 
  margin: 8rem auto; // centers container
  background-color: var(--color-grey-light-2);
  box-shadow: var(--shadow-dark);
  min-height: 50rem;

   @media only screen and (max-width: 75em) {
    margin: 0;
    max-width: 100%;
    width: 100%;
  }
}
</style>

<template>
 <div class="container">

 </div>
</template>

<script>
import HelloWorld from '@/components/HelloWorld.vue'

export default {
  name: 'home',
  components: {
    HelloWorld
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
}
</style>

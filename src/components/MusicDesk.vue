<template>
  <main class="py-5">
      <DeskCard/>
  </main>
</template>

<script>
import DeskCard from '@/components/DeskCard.vue'


export default {
    name: 'MusicDesk',

    components: {
    DeskCard,
  }
}
</script>

<style lang="scss" scoped>

    main{
        height: calc(100vh - 70px);
        background-color: #1e2d3b;
    }

   
</style>
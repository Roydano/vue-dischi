<template>
  <div id="app">
    <Header/>
    <MusicDesk/>
  </div>
</template>

<script>
import Header from '@/components/Header.vue'
import MusicDesk from '@/components/MusicDesk.vue'


export default {
  name: 'App',
  components: {
    Header,
    MusicDesk
  }
}
</script>

<style lang="scss">
@import '@/style/common.scss';
</style>

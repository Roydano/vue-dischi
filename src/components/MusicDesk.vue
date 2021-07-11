<template>
  <main class="py-5">
    <div class="container">
      <div class="row offset-1 justify-content-center offset_right_1">
        <div v-for="(music, index) in musicBox" :key="index" class="col-6 col-md-3 col-lg-auto">
          <DeskCard :song="music"/>
        </div>
      </div>
    </div>
  </main>
</template>

<script>
import axios from 'axios'
import DeskCard from '@/components/DeskCard.vue'


export default {
    name: 'MusicDesk',

    components: {
      DeskCard,
    },

  data(){
    return{
        urlApi: 'https://flynn.boolean.careers/exercises/api/array/music',
        musicBox:''
    }
  },

  created(){
      this.getMusic()
  },

  methods:{
    getMusic(){
      axios
        .get(this.urlApi)
        .then(res =>{
            // console.log(res.data.response);
            this.musicBox = res.data.response

        })
    }
  }
}
</script>

<style lang="scss" scoped>

  .offset_right_1{
        margin-right: 8.33333333%;
    }
   
</style>
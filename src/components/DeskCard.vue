<template>
  <section>
      <div class="container">
          <div class="row offset-1 justify-content-center offset_right_1">
              <div class="col-6 col-md-3 col-lg-auto">
                  
              </div>
          </div>
      </div>
  </section>
</template>

<script>
import axios from 'axios'

export default {
    name: 'DeskCard',

    data(){
        return{
            urlApi: 'https://flynn.boolean.careers/exercises/api/array/music',
            musicsBox:''
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

    .box{
        height: 300px;
        background-color: red;

        .image{
            height: 150px;
            width: 130px;

            img{
                width: 100%;
            }
        }
    }
    

</style>


// v-for="(music, index) in musicsBox" :key="index" 

// {
//             "poster": "https://www.onstageweb.com/wp-content/uploads/2018/09/bon-jovi-new-jersey.jpg",
//             "title": "New Jersey",
//             "author": "Bon Jovi",
//             "genre": "Rock",
//             "year": "1988"
//         },
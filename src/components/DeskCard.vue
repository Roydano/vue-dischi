<template>
  <div class="box my-2 p-3 d-flex flex-column text-center">
      <div class="image">
         <img :src="song.poster" :alt="song.title">
      </div>
      <div class="info_music">
          <h3>{{song.title}}</h3>
          <span>{{song.author}}</span>
          <span>{{song.year}}</span>
      </div>
  </div>
</template>

<script>

export default {
    name: 'DeskCard',
    props: ["song"]

}
</script>

<style lang="scss" scoped>

    

    .box{
        height: 300px;
        background-color: #2e3a46;

        .image{
            height: 150px;
            width: 130px;

            img{
                width: 100%;
            }
        }

        h3{
            font-size: 20px;
            max-width: 130px;
            text-transform: uppercase;
            color: white;
        }

        span{
            max-width: 130px;
            display: block;
            color: #808080;

        }
    }
    

</style>
<template>
  <header class="d-flex align-items-center ps-3">
      <img src="@/assets/spotify-logo.png" alt="spotify logo">
  </header>
</template>

<script>
export default {
    name: 'Header'
}
</script>

<style lang="scss" scoped>

    header{
        height: 70px;
        background-color: #2e3a46;

        img{
            height: 60%;
        }
    }
    
</style>
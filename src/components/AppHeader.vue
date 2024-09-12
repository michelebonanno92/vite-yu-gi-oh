<script>
export default {
  data() {
    return { 
    
    }
  }
}
</script>

<template>
  <header>
   <div class="container d-flex align-items-center">
    <img src="/img/1.jpg" alt="logo">
    <h1>
      Yo-Gi-Oh Api
    </h1>
   </div>
  </header>
</template>

<style lang="scss" scoped>
@use '../assets/scss/partials/variables' as *;

header {
  background-color: $headerBgColor;
  text-align: center;
  padding: 20px 0;
  div > img {
    height: 20px ;
    margin-right: 10px;
  }
}

</style>

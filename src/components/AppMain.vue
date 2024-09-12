<script>
import axios from 'axios' ;

export default {
  data() {
    return { 
        allCards: []
    }
  },
  created() {
    axios
    .get('https://db.ygoprodeck.com/api/v7/cardinfo.php?num=20&offset=0')
    .then((res) => {
        
        this.allCards = res.data.results;

        console.log()
    });

    }
  }
</script>

<template>
    <main>
        <div class="container text-center py-5">
            <div class="row  d-flex  grid gap-4" >
                <div v-for="(card , i) in  allCards" :key="i">
                    ciao
                </div>
            </div>
        </div>

    </main>


</template>


<style lang="scss" scoped>
@use '../assets/scss/partials/variables' as *;

    main {
        background-color: $mainBgColor;
        height: 85vh;
        .container .row div{
            width: calc(100% / 5 - 20px);
            background-color: yellow;
            border: 1px solid black;
            height: 300px;
        }
    }

</style>
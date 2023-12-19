<template lang="">
  <section id='cards-wrapper' class="container">
    <div class="row">
       
        <h2 class="py-3 fs-6">
            Found {{ cardList.length }} cards
        </h2>
    </div>
    <div class="cards row">
        <CardElement  v-for="card in cardList" :key="card.id" :card="card"/>
    </div>

   

  </section>

</template>
<script>
import axios from 'axios';
import CardElement from './CardElement.vue';

export default {
    data (){
        return {
            cardList: [],
            apiUrl: 'https://db.ygoprodeck.com/api/v7/cardinfo.php?num=20&offset=0',
            
        }
    },



    components: {
        CardElement,
    },

    methods: {
        getCards(){
            axios.get(this.apiUrl)
                .then((response) => {
                    console.log(response.data.data);
                    this.cardList = response.data.data
                })
                .catch(function (error) {
                    console.log(error);
                });

        }

    },

    created() {
        this.getCards();

    },

    
   
   
  

    
}
</script>
<style lang="scss" scoped>
@use '../styles/partials/variables' as *;
@use '../styles/partials/mixins' as *;

section#cards-wrapper {
    background-color: white;

    h2{
        background-color: black;
        color: white;
    }
}
    
</style>
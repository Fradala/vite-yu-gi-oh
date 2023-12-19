<template lang="">
  <HeaderYu/>
  <MainYu/>
  
</template>

<script>
import axios from 'axios';
import HeaderYu from './components/HeaderYu.vue';
import MainYu from './components/MainYu.vue'


export default {
  name: 'App',
  components:{
    HeaderYu,
    MainYu,
    
    
  },

  data() {
    return{
      carte: [],
      
    }
    
  },

  methods: {
    getCarte(){
      axios.get('https://db.ygoprodeck.com/api/v7/cardinfo.php?num=20&offset=0')
      .then((response) => {
        console.log(response.data.data);
        this.carte = response.data.data;
        
      })
      .catch(function (error){
        console.log(error);
      });
    }

  },

  created() {
    this.getCarte();
  }
  
}
</script>
<style lang="scss">
    @use './styles/general.scss' as *;
</style>
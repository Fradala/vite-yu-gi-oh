<template lang="">
  
  <HeaderYu/>
  <MainYu/>
</template>

<script>

import HeaderYu from './components/HeaderYu.vue';
import MainYu from './components/MainYu.vue';
export default {
  name: 'App',
  components:{
    HeaderYu,
    MainYu,
    
  }
  
}
</script>
<style lang="scss">
    @use './styles/general.scss' as *;
</style>
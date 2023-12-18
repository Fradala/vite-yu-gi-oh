<template lang="">
   <section id="searchyu">
        <article v-for="carte in listacarte">
            <p>
                {{ carte.name }}
            </p>

        </article>
   </section>

</template>
<script>
import { store } from '../js/store.js' 
export default {

    
    data() {
        return{
            store,
        }
    },

   
  

    
}
</script>
<style lang="scss" scoped>
@use '../styles/partials/variables' as *;
@use '../styles/partials/mixins' as *;
    
</style>
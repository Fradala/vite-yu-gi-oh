<template lang="">
   <section id="searchyu" class="conteiner">
        <div class="row">
            <article v-for="carte in listacarte" class="col-md-4 col-lg-2">
                <img src="" alt="">
                <p>
                    {{ carte.name }}
                </p>

        </article>
        </div>
        
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

    props: {
        listacarte: {
            type: Array,
            required: true,
        }
    }

   
  

    
}
</script>
<style lang="scss" scoped>
@use '../styles/partials/variables' as *;
@use '../styles/partials/mixins' as *;
    
</style>
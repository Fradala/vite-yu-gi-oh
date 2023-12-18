<template lang="">
   <section id="searchyu">
        <article v-for="carte in listacarteyu">
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

    props: {
        listacarteyu: {
            type: Array,
            required: true,
        }
    }

    
}
</script>
<style lang="">
    
</style>
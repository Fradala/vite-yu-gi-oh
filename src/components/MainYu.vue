<template lang="">
    <main>
        <CardsWrapper/>

    </main>
   
    
</template>
<script>
import CardsWrapper from './CardsWrapper.vue';
export default {
    components: {
        CardsWrapper,
    }
    
}
</script>
<style lang="scss" scoped>
@use '../styles/partials/variables' as *;
@use '../styles/partials/mixins' as *;

main{
    padding: 4rem;
    background-color: #d48f38;
}
    
</style>
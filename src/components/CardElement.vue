<template lang="">
   <article class="p-0">
        <section class="image">
            <img :src="card.card_images[0].image_url" alt="">
        </section>

        <p class="text-white text-uppercase fs-6 fw-bold">
            {{ card.name }}
        </p>
        <p>
            {{ card.archetype }}
        </p>


   </article>
</template>
<script>
export default {
    props:{
        card: {
            type: Object,
            required: true
        }

    },
}
</script>
<style lang="scss" scoped>

article{
    background-color: #d48f38;
    width: calc(100% / 5 - 1rem);
    margin-left: .5rem;
    margin-right: .5rem;
    margin-bottom: 1rem;
    text-align: center;


    img{
        width: 100%;
    }

    
}
    
</style>
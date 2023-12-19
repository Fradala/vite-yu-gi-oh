<template lang="">
    <div>
        <div class="input-group mb-3">
            <span class="input-group-text" id="basic-addon1">Type of cards</span>
            <input type="text" class="form-control" placeholder="Type of cards" aria-label="Type of cards"
             aria-describedby="basic-addon1" @keyup.enter="$emit('search')" v-model="store.searchType">
        </div>
 
    </div>
    
</template>
<script>
import { store } from '../js/store';
export default {
    data() {
        return{
            store,
        }
    }
    
}
</script>
<style lang="">
    
</style>
<script>
export default {
    data() {
        return {
            inputText: "",
        }
    }
}
</script>

<template>
    <div class="cardsearch-div">
        <input class="search" v-model="inputText" @input="$emit('updateSearch', inputText)" placeholder="Search a card name..." width=500px>
    </div>
</template>

<style>
.search {
    display: flex;
    width: 35.8rem;
    height: 30px;
    margin-bottom: 10px;
    
}
</style>
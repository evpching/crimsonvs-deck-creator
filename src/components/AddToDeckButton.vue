<script>
export default {
    data() {
        return {
            selectedCard: "",
        }
    },
    props: {
        buttonName: String
    }
}
</script>

<template>
     <button @click="$emit('addSelected', selectedCard)" class="addtodeck-button" type="button">{{ buttonName ? `Click to add "${buttonName}" to the deck.` : `Select a card to add to the deck!` }}</button> 
</template>

<style>
.addtodeck-button {
    margin-top: 10px;
    height: 40px;
    font-family: 'Lucida Sans', 'Lucida Sans Regular', 'Lucida Grande', 'Lucida Sans Unicode', Geneva, Verdana, sans-serif;
}

</style>
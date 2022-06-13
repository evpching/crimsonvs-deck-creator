<script>

export default {
  data() {
    return {
      numberToDisplay: 24,
      selectedCard: {},
    }
  },
  props: {
    cardList: Array
  }
}

</script>

<template>
    <div class="cardlist-div">
        <select class="cardlist-select" v-model="selectedCard" @change="$emit('updateSelected', selectedCard)" :size="numberToDisplay">
          <option v-for="card in cardList">[{{ card.id.toString().padStart(3, '0') }}] {{ card.type }} / {{ card.name }}</option>
        </select>
    </div>
</template>

<style>

.cardlist-div {
  display: flex;
  flex-direction: column;
  color: white;
  font-family: 'Lucida Sans', 'Lucida Sans Regular', 'Lucida Grande', 'Lucida Sans Unicode', Geneva, Verdana, sans-serif;
}

.cardlist-select {
  background-color: rgb(48, 48, 48);
  color: white;
  font-family: 'Lucida Sans', 'Lucida Sans Regular', 'Lucida Grande', 'Lucida Sans Unicode', Geneva, Verdana, sans-serif;

}

</style>
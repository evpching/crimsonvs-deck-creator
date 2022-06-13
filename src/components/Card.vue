<script>
export default {
    props: {
      card: {}
  }
}

</script>

<template>
  <div class="card-grid">
    <p class="grid-stats">{{ card.name }}</p>
		<button @click="$emit('removeCard', card)" class="grid-button" type="button">Remove from Deck</button> 
  </div>
</template>

<style>
.card-grid {
	display: grid;
	grid-template-areas: 
		"stats   stats"
		"img   img"
		"info   info"
		"buttons buttons";

	grid-template-rows: 200px 1fr 1fr 1fr;

  border-color: coral;
  border-style: outset;

	background-color:rgb(48, 48, 48);

	animation-name: card-moveupwards;
  animation-duration: 0.5s;

}

.grid-stats {
	grid-area: stats;
	color: white;
}

.grid-img {
	grid-area: img;
}

.grid-info {
	grid-area: info;

}

.grid-button {
	grid-area: buttons;
	margin-top: 200px;
	display: flex;
	height: 40px;
	align-items: center;
	justify-content: center;
}

@keyframes card-moveupwards {
  from {margin-bottom: 400px;}
  to   {margin-bottom: 0px;}
}
</style>
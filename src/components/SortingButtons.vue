<template>
	<div class="grid-container-sortingbuttons">	
		<button type="button">Sort by HP</button> 
		<button type="button">Sort by AP</button> 
		<button type="button">Sort by Charisma</button> 
		<button type="button">Sort by Rarity</button> 
	</div>
</template>

<style>
.grid-container-sortingbuttons {
	display: grid;
	grid-template-areas: "button button button button";
}
</style>
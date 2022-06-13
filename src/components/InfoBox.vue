<template>
	<div class="infobox-grid">
			<img class="infobox-image" src="https://puu.sh/J5sw9/a524eddde6.png">
			<ul class="infobox-info">
				<li>Hi there!</li>
				<li>Welcome to my vue app!</li>
			</ul>
	</div>
</template>

<style>
.infobox-grid {
	margin-top: 117px;
	display: grid;
	grid-template-areas: 
    "image info";
	grid-template-columns: .1fr 1fr;
	background-color: rgb(48, 48, 48);
}

.infobox-image {
	grid-area: image;
}

.infobox-info {
	grid-area: info;
	color: white;
}
</style>
<script setup>
import Banner from './components/Banner.vue'
import AddToDeckButton from './components/AddToDeckButton.vue'
import SortingButtons from './components/SortingButtons.vue'
import CategoryButtons from './components/CategoryButtons.vue'
import InfoBox from './components/InfoBox.vue'
import CardList from './components/CardList.vue'
import CardSearch from './components/CardSearch.vue'
import Card from './components/Card.vue'
</script>

<script>
export default {
  data() {
    return {
      cardList: [{"id":1,"type":"General","name":"Haseo at Dawn (黎明のハセヲ)","junctionability":"None","charisma":12,"hp":16,"ap":3,"trinity":"Assault","rarity":"Ultra Rare"},{"id":2,"type":"General","name":"Kite (カイト)","junctionability":"None","charisma":10,"hp":16,"ap":3,"trinity":"Assault","rarity":"Super Rare"},{"id":3,"type":"General","name":"Haseo the Black Rogue (黒衣の錬装士ハセヲ)","junctionability":"None","charisma":9,"hp":16,"ap":4,"trinity":"Assault","rarity":"Super Rare"},{"id":4,"type":"General","name":"BlackRose (ブラックローズ)","junctionability":"None","charisma":11,"hp":11,"ap":3,"trinity":"Assault","rarity":"Rare"},{"id":5,"type":"General","name":"Haseo the Terror of Death (死の恐怖ハセヲ)","junctionability":"None","charisma":6,"hp":20,"ap":4,"trinity":"Assault","rarity":"Rare"},{"id":6,"type":"General","name":"Pi - Raven (レイヴン　パイ)","junctionability":"None","charisma":8,"hp":17,"ap":3,"trinity":"Assault","rarity":"Common"},{"id":7,"type":"General","name":"Balmung (バルムンク)","junctionability":"None","charisma":7,"hp":15,"ap":4,"trinity":"Assault","rarity":"Common"},{"id":8,"type":"General","name":"Tabby - Twilight Brigade (黄昏の旅団　タビー)","junctionability":"None","charisma":12,"hp":14,"ap":1,"trinity":"Assault","rarity":"Common"},{"id":9,"type":"General","name":"Degenerating Haseo (堕とされしハセヲ)","junctionability":"None","charisma":7,"hp":23,"ap":2,"trinity":"Assault","rarity":"Common"},{"id":10,"type":"General","name":"Shino - Twilight Brigade (黄昏の旅団　志乃)","junctionability":"None","charisma":14,"hp":16,"ap":2,"trinity":"Shield","rarity":"Ultra Rare"},{"id":11,"type":"General","name":"Sakisaka - Twilight Brigade (黄昏の旅団　匂坂)","junctionability":"None","charisma":10,"hp":20,"ap":2,"trinity":"Shield","rarity":"Ultra Rare"},{"id":12,"type":"General","name":"Haseo Counterattacks (反撃のハセヲ)","junctionability":"None","charisma":8,"hp":23,"ap":3,"trinity":"Shield","rarity":"Super Rare"},{"id":13,"type":"General","name":"Gaspard - Canard (カナード　ガスパー)","junctionability":"None","charisma":11,"hp":15,"ap":2,"trinity":"Shield","rarity":"Rare"},{"id":14,"type":"General","name":"Atoli - Moon Tree (月の樹　アトリ)","junctionability":"None","charisma":10,"hp":17,"ap":2,"trinity":"Shield","rarity":"Rare"},{"id":15,"type":"General","name":"Sakubo - Trifle (トライフル　朔望)","junctionability":"None","charisma":10,"hp":10,"ap":2,"trinity":"Shield","rarity":"Common"},{"id":16,"type":"General","name":"Orca (オルカ)","junctionability":"None","charisma":9,"hp":11,"ap":4,"trinity":"Shield","rarity":"Common"},{"id":17,"type":"General","name":"Raid of New Punishers (新米撃剣士レイド)","junctionability":"None","charisma":6,"hp":29,"ap":1,"trinity":"Shield","rarity":"Common"},{"id":18,"type":"General","name":"Ovan the Wanderer (流雄のオーヴァン)","junctionability":"None","charisma":12,"hp":12,"ap":4,"trinity":"Snipe","rarity":"Ultra Rare"},{"id":19,"type":"General","name":"Tri-Edge (三爪痕)","junctionability":"None","charisma":5,"hp":25,"ap":5,"trinity":"Snipe","rarity":"Super Rare"},{"id":20,"type":"General","name":"Endrance the Exquisite (麗のエンデュランス)","junctionability":"None","charisma":13,"hp":10,"ap":3,"trinity":"Snipe","rarity":"Super Rare"},{"id":21,"type":"General","name":"Kuhn - Raven (レイヴン　クーン)","junctionability":"None","charisma":12,"hp":10,"ap":2,"trinity":"Snipe","rarity":"Rare"},{"id":22,"type":"General","name":"Bordeaux the Mad Blade (凶刃のボルドー)","junctionability":"None","charisma":8,"hp":24,"ap":2,"trinity":"Snipe","rarity":"Rare"},{"id":23,"type":"General","name":"Ovan the Twilight (黄昏の徒オーヴァン)","junctionability":"None","charisma":11,"hp":8,"ap":3,"trinity":"Snipe","rarity":"Common"},{"id":24,"type":"General","name":"Mistral (ミストラル)","junctionability":"None","charisma":10,"hp":14,"ap":1,"trinity":"Snipe","rarity":"Common"},{"id":25,"type":"General","name":"Silabus - Canard (カナード　シラバス)","junctionability":"None","charisma":9,"hp":18,"ap":2,"trinity":"Snipe","rarity":"Common"},{"id":86,"type":"General","name":"Haseo the Silver Dual Gunner","junctionability":"Shooting Squad","charisma":12,"hp":14,"ap":3,"trinity":"Assault","rarity":"Ultra Rare"},{"id":87,"type":"General","name":"Bordeaux in Distress","junctionability":"AIDA Berserk","charisma":6,"hp":22,"ap":4,"trinity":"Assault","rarity":"Ultra Rare"},{"id":88,"type":"General","name":"Alkaid - Icolo","junctionability":"Emperor's Pride","charisma":10,"hp":12,"ap":3,"trinity":"Assault","rarity":"Super Rare"},{"id":89,"type":"General","name":"Cold-Hearted Saku","junctionability":"AIDA Corrosion","charisma":12,"hp":16,"ap":2,"trinity":"Assault","rarity":"Super Rare"},{"id":90,"type":"General","name":"Kaede - Moon Tree","junctionability":"Whirlwind Assault","charisma":10,"hp":14,"ap":2,"trinity":"Assault","rarity":"Rare"},{"id":91,"type":"General","name":"Sirius - Icolo","junctionability":"Emperor's Pride","charisma":9,"hp":10,"ap":3,"trinity":"Assault","rarity":"Rare"},{"id":92,"type":"General","name":"Sophora - Moon Tree","junctionability":"Mobilize the Troops","charisma":6,"hp":8,"ap":4,"trinity":"Assault","rarity":"Common"},{"id":93,"type":"General","name":"Twilight Knight Piros the 3rd","junctionability":"Cross Counter","charisma":8,"hp":12,"ap":2,"trinity":"Assault","rarity":"Common"},{"id":94,"type":"General","name":"Beast Awakening Haseo","junctionability":"Charge Ahead","charisma":9,"hp":18,"ap":2,"trinity":"Assault","rarity":"Common"},{"id":95,"type":"General","name":"Zelkova - Moon Tree","junctionability":"Kaede's Guard","charisma":15,"hp":17,"ap":0,"trinity":"Shield","rarity":"Ultra Rare"},{"id":96,"type":"General","name":"Sakaki Lost in Ambition","junctionability":"AIDA Berserk","charisma":8,"hp":18,"ap":4,"trinity":"Shield","rarity":"Ultra Rare"},{"id":97,"type":"General","name":"Azure Orca","junctionability":"Defensive Stance","charisma":6,"hp":16,"ap":4,"trinity":"Shield","rarity":"Super Rare"},{"id":98,"type":"General","name":"Avatar Awakening Haseo","junctionability":"Gathering of the Strong","charisma":11,"hp":10,"ap":3,"trinity":"Shield","rarity":"Super Rare"},{"id":99,"type":"General","name":"Yata - Raven","junctionability":"Ingenious Scheme","charisma":10,"hp":12,"ap":2,"trinity":"Shield","rarity":"Rare"},{"id":100,"type":"General","name":"Bo - Trifle","junctionability":"Defensive Stance","charisma":12,"hp":12,"ap":1,"trinity":"Shield","rarity":"Rare"},{"id":101,"type":"General","name":"Sakaki - Moon Tree","junctionability":"Shield Protection","charisma":12,"hp":8,"ap":1,"trinity":"Shield","rarity":"Common"},{"id":102,"type":"General","name":"Hiiragi - Moon Tree","junctionability":"Mobilize the Troops","charisma":11,"hp":14,"ap":1,"trinity":"Shield","rarity":"Common"},{"id":103,"type":"General","name":"Tri-Edge Ovan","junctionability":"AIDA Berserk","charisma":7,"hp":20,"ap":6,"trinity":"Snipe","rarity":"Ultra Rare"},{"id":104,"type":"General","name":"Gabi - Kestrel","junctionability":"Gabi's Call","charisma":11,"hp":16,"ap":4,"trinity":"Snipe","rarity":"Ultra Rare"},{"id":105,"type":"General","name":"Azure Balmung","junctionability":"Charge Ahead","charisma":6,"hp":12,"ap":5,"trinity":"Snipe","rarity":"Super Rare"},{"id":106,"type":"General","name":"Card King Gaspard","junctionability":"Change Ring","charisma":12,"hp":12,"ap":2,"trinity":"Snipe","rarity":"Super Rare"},{"id":107,"type":"General","name":"Taihaku - Icolo","junctionability":"Demon Sword Maxwell","charisma":7,"hp":10,"ap":4,"trinity":"Snipe","rarity":"Rare"},{"id":108,"type":"General","name":"Antares - Icolo","junctionability":"Emperor's Pride","charisma":8,"hp":12,"ap":3,"trinity":"Snipe","rarity":"Rare"},{"id":109,"type":"General","name":"Nala - Moon Tree","junctionability":"Promised Discretion","charisma":9,"hp":10,"ap":12,"trinity":"Snipe","rarity":"Common"},{"id":110,"type":"General","name":"Matsu - Moon Tree","junctionability":"Snipe Thunder","charisma":7,"hp":10,"ap":3,"trinity":"Snipe","rarity":"Common"}],
      cardToSearch: "",
      selectedCard: {},
      deck: []
    }
  },
  methods: {
    setCardToSearch( $event ) {
      this.cardToSearch = $event
      console.log( this.cardToSearch )
    },
    setSelectedCard( $event ) {
      let cardName = $event.split("/ ")[1]
      this.selectedCard = this.cardList.find(card => card.name == cardName)
      //this.deck.push(this.cardList.find(card => card.name == cardName))
      console.log(this.selectedCard)
    },
    addSelectedCard() {
      console.log("add called")
      if (!this.deck.includes(this.selectedCard) && this.deck.length < 4 && this.selectedCard) this.deck.push(this.selectedCard)
      console.log({ deck: this.deck })
    },
    removeCard( $event ) {
      console.log($event)
      this.deck = this.deck.filter(card => card != $event)
    }
  },
  computed: {
    filteredList() {
      return this.cardList.filter(card => { return card.name.toLowerCase().includes(this.cardToSearch.toLowerCase()) })
    }
  },
  components: {
    Banner,
    AddToDeckButton,
    SortingButtons,
    CategoryButtons,
    InfoBox,
    CardList,
    CardSearch,
    Card
  }
}
</script>


<template>
  <div class="grid-container">
    <div class="grid-banner"> <Banner /> </div>
    <div class="grid-banner-navmenu"> <Banner /> </div>
    <div class="grid-topbar-search">  </div>
    <div class="grid-menu"> 
      <CardSearch @updateSearch="setCardToSearch" /> 
      <CardList @updateSelected="setSelectedCard" :cardList="filteredList"/> 
      <AddToDeckButton @addSelected="addSelectedCard" :buttonName="selectedCard.name"/>
      <h2 style="color:white">Sorting Options</h2>
      <CategoryButtons />
      <SortingButtons />
    </div>
    <div class="grid-content"> 
      <Card @removeCard="removeCard" v-for="card in deck" :card="card"/> 
    </div>
    <div class="grid-info">
      <InfoBox />
    </div>
  </div>
</template>

<style>

.grid-container {
  display: grid;
  grid-template-areas: 
    "banner banner    banner"
    "menu   content   content  "
    "menu   info   info";

  grid-template-columns: repeat( 2, minmax(600px, 600px) );
  grid-template-rows: 40px 450px 450px;

  position: fixed;
}

.grid-topbar-search {
  grid-area: 2 / 1;
}

.grid-info {
  grid-area: info;
  margin: 10px;
}

.grid-menu {
  grid-area: menu;
  display: flex;
  margin: 10px;
  flex-direction: column;
}

.grid-content {
  grid-area: content;
  margin: 10px;
  gap: 10px;
  display: grid;
  grid-template-areas: 
  "card card card card";
  grid-template-columns: repeat( 4, minmax(300px, 300px) );
  grid-template-rows: repeat( 4, minmax(400px, 400px) );
}

.grid-banner {
  grid-area: 1 / 1 / span 1 / span 1;
  background-color: aquamarine;
  text-align:center;
}

.grid-banner-navmenu {
  grid-area: 1 / 2 / span 1 / span 2;
  background-color: aquamarine;
  text-align: center;
}

body {
  background-color: rgb(24, 24, 24);
}

</style>
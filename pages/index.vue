<template>
  <div class="container">
    <div>
    <h2>Add God</h2>
	  <addGod />
    </div>
  </div>
</template>

<script>
import AddGod from '~/components/AddGod.vue';

// const Data = [
// 	{
// 		name: "Zeus",
// 		nickname: "God of lightning",
// 		description: "Ubergod that rules over all other gods, resides on mount olympus",
// 		commandments: "Hump many women and lightning is cool. Cheat on waifu's for new waifu's. Create demihumans cuz of thirst",
// 		alignment: "Good",
// 		followers: "Ancient greek people",
// 		domain: "Thunder, lightning and pikachu"
// 	}, {
// 		name: "Poseidon",
// 		nickname: "God of ocean",
// 		description: "Ubergod, but less Ubergod than Zeus but still uber. Resides in oceans. Loves water",
// 		commandments: "Hump many women and water is cool. Cheat on waifu's for new waifu's. Create demihumans cuz of thirst",
// 		alignment: "Good",
// 		followers: "Ancient greek people",
// 		domain: "Water and blastoise"
// 	}
// ]

export default {
  components: {
	AddGod
  }
}
</script>
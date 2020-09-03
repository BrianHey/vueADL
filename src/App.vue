<template>
	<div>
		<input v-model="nombre" type="text" />
		<!--  <button @click="buscar">Pokémon</button>
 <div>
    <img :src="imagen" alt="">
    <h6>{{nombrePokemon}}</h6>
    <p>{{movimientos}}</p>
  </div> -->
	</div>
</template>

<script>
export default {
	name: 'app',
	data() {
		return {
			nombre: ' ',
			pokemon: {},
		};
	},
	created() {
		this.buscarPokemon();
	},
	methods: {
		buscarPokemon() {
			fetch('https://pokeapi.co/api/v2/pokemon/ditto')
				.then(function(response) {
					return response.json();
				})
				.then((myJson) => {
          console.log(myJson);
           this.pokemon = myJson
        });
		},
	},
};
</script>

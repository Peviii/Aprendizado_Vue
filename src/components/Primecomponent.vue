<template>
	<div>
	<h1>Olá Vue</h1>
	<p>Meu nome é {{nome}} e trabalho como {{profissao}}</p>
	<MultiEventos />
	<Reusable />
	</div>
</template>

<script>
	import MultiEventos from './MultiEventos.vue';
	import Reusable from "./Reusable.vue";
	export default{
		name: 'Primecomponent',
		components: {
			MultiEventos,
			Reusable
		},
		data(){
			return{
				nome:"Pedro",
				profissao:"Programador"
			}
		}
	}
</script>
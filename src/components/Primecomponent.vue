<template>
	<h1>Olá Vue</h1>
	<p>Meu nome é {{nome}} e trabalho como {{profissao}}</p>
	<MultiEventos />
</template>

<script>
	import MultiEventos from './MultiEventos.vue';
	export default{
		name: 'Primecomponent',
		components: {
			MultiEventos
		},
		data(){
			return{
				nome:"Pedro",
				profissao:"Programador"
			}
		}
	}
</script>
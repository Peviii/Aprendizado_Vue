<template>
	<div>
		<button @click="primeiro(txt1,$event),segundo(txt2,$event),terceiro()">
		Ativar multiplos eventos
        </button>
		<p>{{multi_eventos}}</p>
	</div>
</template>
<script>
	export default{
       name:'MultiEventos',
        data(){
            return{
             multi_eventos:"",
             txt1: "primeiro evento",
             txt2: "segundo evento"
            }
        },
		methods:{
			primeiro(txt){
				this.multi_eventos = txt;
			},
			segundo(txt){
				setTimeout(()=>this.multi_eventos = txt,500)
			},
			terceiro(){
				setTimeout(()=>this.multi_eventos = "",1500)
			}
		}
	}
</script>
<style scoped>
	div{
      margin: 100px;	
	}
</style>
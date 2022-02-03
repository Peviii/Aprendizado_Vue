<template>
	<div>
		<p v-if="is_working">Estou trabalhando no momento.</p>
		<p v-else>estou em busca de novas oportunidades</p>
		<p>Utilizo as Seguintes tecnologias para back-end:</p>
		<ul>  
            <li v-for="(technology,index) in backend_tech" v-bind:key="index">
               {{technology}}
            </li>
        </ul>
        <p>Utilizo as seguintes tecnologias para front-end:</p>
        <ul>
            <li v-for="technology in frontend_tech" :key="technology.id">
              {{technology.language}}
            </li>
        </ul>
        <div>
           <button @click="showEmail">{{ textButton }}</button>
        </div>
        <p v-show="show_email">Mande uma mensagem para {{ email }}</p>
        <p class="teste">Para acessar meu portfolio <a v-bind:href="my_link" target="_blank">basta clicar aqui</a></p>
		<Picture />
	</div>
</template>
<script>
	import Picture from "./Picture.vue"
	export default{
		name:'Info',
		components:{
			Picture
		},
		data(){
			return{
				is_working: false,
				show_email:false,
				email: 'Pedro@email.com',
				my_link:'https://google.com',
				textButton:'mostrar email',
				backend_tech: ["JavaScript","PHP","Python"],
				frontend_tech: [
                  {id:1,language:"HTML"},
                  {id:2,language:"CSS"},
                  {id:3,language:"Vue"}
				]
			}
		},
		methods:{
			showEmail(){
				this.show_email = !this.show_email;	
				if(!this.show_email){
					this.textButton = 'mostrar email';
				}else{this.textButton = 'esconder email';}
			}
		}
	}
</script>
<style>
	.paragrafo-pai{
       color: red;
	}
</style>
<template>
	<ul>
		<li><a href="#">home</a></li>
		<li><a href="#">projetos</a></li>
		<li><a href="#">contato</a></li>
		<li><a href="#">dashboard</a></li>
	</ul>
</template>
<script>
	export default{
		name:'header'
	}
</script>
<style scoped>
	ul{
		list-style: none;
        display: flex;
        background: #999;
	}
	li{
		margin-right: 10px;
	}
	a{
		color: #DDD;
		text-decoration: none;
		transition: 1s;
	}
	a:hover{
		color: turquoise;
	}
</style>
<template>
	<img :src="avatar" :alt="descript">
</template>
<script>
	export default{
		name: 'Picture',
		data(){
            return{	
              avatar:"/img/avatar.png",
              descript:"Pietro Capuletto Montechio"
            }
        }
	}
</script>
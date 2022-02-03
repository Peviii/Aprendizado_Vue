<template>
	<img :src="avatar" :alt="descript">
	<Reusable />
</template>
<script>
  import Reusable from './Reusable.vue';

	export default{
		name: 'Picture',
		components:{
			Reusable
		},
		data(){
            return{	
              avatar:"/img/avatar.png",
              descript:"Pietro Capuletto Montechio"
            }
        }
	}
</script>
<template>
  <div>
     <Loader v-if="getLoader" class="text-center"> </Loader> 
  </div>
</template>

<script>

import Loader from "./Loader.vue"

export default {
    computed:{
     getLoader() {
       return this.$store.getters.getLoader
     },
    },

    created(){
        this.$store.dispatch('destroyToken')
        .then(response => {
             if(response.status == 200){
             this.$router.push({ name: 'home'});
         }

        })
        .catch(error => {
           this.$router.push({ name: 'home'});
        })
    },
    components: { Loader }
}

</script>
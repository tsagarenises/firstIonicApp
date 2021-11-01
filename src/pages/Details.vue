<template>
    <base-layout :pageTitle="loadedMemory ? loadedMemory.title:'loading...'" deafultBack="/memories">
        <h2 v-if="!loadedMemory">cant find memory</h2>
        <h2 v-else>loaded it</h2>
    </base-layout>
</template>

<script>
export default {
     data(){
         return{
            memoryId: this.$route.params.id,
         };
         
     },
     computed:{
         loadedMemory(){
             return this.$store.getters.memory(this.memoryId);
         }
     },
    //  watch:{
    //      '$route'(currentRoute){
    //          this.memoryId=currentRoute.params.id;
    //      }
    //  }
}
</script>
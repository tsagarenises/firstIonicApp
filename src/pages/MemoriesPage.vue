<template>
    <base-layout :pageTitle="'TODAYS ACTIVITIES'">
            <ion-list>
                <ion-item 
                v-for="memory in memories"
                :router-link="`/memories/${memory.id}`" 
                :key="memory.id">
                <ion-thumbnail>
                <ion-img :src="memory.img" :alt="memory.title"></ion-img>
                </ion-thumbnail>
                <ion-label>
                {{memory.title}}
                </ion-label>
                </ion-item>
             </ion-list>
    </base-layout>
</template>

<script>
import { IonList, IonItem, IonImg, IonThumbnail, IonLabel } from '@ionic/vue';
export default {
    components:{
        IonList,
        IonItem,
        IonImg,
        IonLabel,
        IonThumbnail
    },
    computed:{
        memories(){
            return this.$store.getters.memories;
        }
    }
}; 
</script>
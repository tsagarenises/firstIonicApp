<template>
     <ion-page>
        <ion-header>
            <ion-toolbar>
                <ion-buttons slot="start">
                    <ion-back-button :default-href="deafultBack"></ion-back-button>
                </ion-buttons>
                <ion-title>{{ pageTitle}}</ion-title>
            </ion-toolbar>    
        </ion-header>

        <ion-content>
            <slot/>
        </ion-content>
    </ion-page>
</template>

<script>
    import {IonPage, IonToolbar, IonButtons, IonHeader, IonContent, IonTitle, IonBackButton} from '@ionic/vue';
export default {
    props:['pageTitle', 'deafultBack'],
    components:{
        IonPage,
        IonToolbar,
        IonHeader,
        IonTitle,
        IonContent,
        IonBackButton,
        IonButtons
    }
}
</script>
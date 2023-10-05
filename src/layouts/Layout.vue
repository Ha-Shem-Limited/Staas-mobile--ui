<template>
    <ion-page>
        <ion-header >
            <ion-toolbar>
                <ion-buttons slot="start">
                    <img src="../assets/staas-blue.svg" alt="logo" >
                </ion-buttons>


                <ion-buttons slot="end">
                    <img src="../assets/user.svg" alt="user" >
                </ion-buttons>
            </ion-toolbar>
        </ion-header>

        <slot></slot>
       
    </ion-page>
</template>

<script setup>
    import {IonContent, IonPage, IonToolbar, IonButtons } from '@ionic/vue'
</script>

<style scoped lang="scss">
    ion-toolbar {
        --background: white;
        --padding-bottom: 1.25rem;
        --padding-top: 1.25rem;
        --padding-start: 1.25rem;
        --padding-end: 1.25rem;
        --border-color: white;
    }

</style>
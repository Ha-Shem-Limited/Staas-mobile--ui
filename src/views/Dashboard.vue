<template>
    <ion-content class="dashboard">
       <div class="dashboard__user">
            <h4>Hello</h4>
            <h1>Annabel</h1>
       </div>

       <ion-card id="banner">
            <ion-card-content id="banner__content">
                <h1>TEST</h1>
                <div></div>

            </ion-card-content>
       </ion-card>

       <div class="dashboard__cards">
            <DashboardCard  color="success" title="Good Morning" message="Ready for today’s work?" >
                <template #icon>
                    <img src="../assets/sign-in.svg" alt="Sign In Icon" >
                </template>
            </DashboardCard>

            <DashboardCard  color="danger" title="Goodbye" message="Done for the day?" >
                <template #icon>
                    <img src="../assets/goodbye.svg" alt="Sign In Icon" >
                </template>
            </DashboardCard>

            <DashboardCard  color="dark" title="Staff Movement" message="Stepping Out/Resuming back?" >
                <template #icon>
                    <img src="../assets/movement.svg" alt="Sign In Icon" >
                </template>
            </DashboardCard>
       </div>

       
    </ion-content>
</template>


<script setup>
    import { IonContent, IonText, IonCard, IonCardContent } from '@ionic/vue';
    import DashboardCard from '../components/DashboardCard.vue';
</script>

<style scoped lang="scss">
    @use '../partials';
    ion-content {
        --padding-bottom: 1.25rem;
        --padding-top: 6.25rem;
        --padding-start: 1.25rem;
        --padding-end: 1.25rem;
    }

    #banner {
        box-shadow: none;
        height: 10rem;
        position: relative;    
    }

    #banner__content {
        padding: 1rem 2.4537rem .785rem 1rem;
        height: 9.25rem;
        background: linear-gradient(281.42deg, #000066 -7.49%, #010137 107.95%);
        border-radius: 10px;



        & > div {
            position: absolute;
            background: #D9D9FF;
            width: 95%;
            height: 9.25rem;
            bottom: -.5rem;
            right: 0;
            left: 0;
            z-index: -1;
            margin: auto;
            border-radius: 10px;
        }
    }

    .dashboard {
        display: flex;
        flex-direction: column;
        row-gap: 2rem;

        &__user {
            margin-bottom: 2rem;
             & >  h1, h4 {
                padding: 0;
                margin: 0;
             }

             & >  h4 {
                @include partials.button-text;
                font-weight: 400;
             }

             & > h1 {
                @include partials.large-text;
             }
        }


        &__cards {
            display: flex;
            flex-direction: column;
            row-gap: .5rem;
            margin-top: 3.125rem;
        }

    }
</style>
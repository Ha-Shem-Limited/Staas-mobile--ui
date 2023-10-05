<template>
    <ion-content :fullscreen="true">
        <div class="onboarding">
          <img src="../assets/staas.svg" alt="App Logo">
          <form class="onboarding-form">
            <h1>Activation</h1>


            <ion-input class="onboarding-form__email" placeholder="Enter your email address" fill="outline" label="Email Address" label-placement="stacked" inputmode="email"></ion-input>
            
            <ion-button class="onboarding-form__submit">Confirm</ion-button>
          </form>
        </div>
    </ion-content>
</template>

<script setup lang="ts">
  import { IonContent, IonHeader, IonPage, IonTitle, IonToolbar, IonButton, IonInput, IonImg } from '@ionic/vue';
</script>

<style scoped lang="scss">


  @use '../partials';

  @keyframes animate-bg {
    0% {
      height: 100vh;
    }
    50% {
      height: 60vh;
    }
    70% {
      height: 40vh;
    }

    100% {
      height: 20.0625rem;
    }
  }
  .onboarding {
    width: 100%;
    height: 20.0625rem;
    border-radius: 0rem 0rem .625rem .625rem;
    background: linear-gradient(281.42deg, #000066 -7.49%, #010137 107.95%);
    position: relative;
    display: flex;
    justify-content: center;
    align-items: center;
    animation: animate-bg 2s;

    & > img {
      width: 7.5625rem;
      height: 8.375rem;
    }


    &-form {
      position: absolute;
      width: 80%;
      height: max-content;
      border-radius: .625rem;
      background: white;
      left: 0;
      right: 0;
      top: 17.1875rem;
      margin: auto;
      display: flex;
      flex-direction: column;
      padding: 1.5rem 1.125rem;
      row-gap: 1.875rem;

    

      & > h1 {
        align-self: center;
        margin: 0;
        padding: 0;
        font-size: 16px;
        font-weight: 500;
        line-height: 18px;
        letter-spacing: 0em;
      }

      &__submit {
        width: 100%;
        height: 3.25rem;
        border-radius: 7px;
        color: white;
        @include partials.button-text;

      }
    }

  }


  ion-content {
    --background: #DBDBDB;
  }

</style>

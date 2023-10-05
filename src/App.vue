<template>
  <ion-app>
    <component :is="$route.meta.layout || 'ion-page'">
      <ion-router-outlet />
    </component>
  </ion-app>
</template>

<script setup lang="ts">
import { IonApp, IonRouterOutlet, IonPage } from '@ionic/vue';
</script>

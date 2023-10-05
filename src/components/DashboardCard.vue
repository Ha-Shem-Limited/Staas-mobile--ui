<template>
    <ion-card >
        <ion-card-content>

            <div class="card__icon">
                <slot name="icon"></slot>
            </div>

            <div class="card__right">
                <div class="card__right-message">
                    <h1>{{ title }}</h1>
                    <h4>{{ message }}</h4>
                </div>


                <ion-button>Sign in</ion-button>

            </div>
        </ion-card-content>
    </ion-card>
</template>

<script setup>
    import { IonCard, IonCardContent, IonButton, IonItem } from '@ionic/vue';
    import { defineEmits, defineProps } from 'vue';


    const $emit = defineEmits(['clicked']);

    defineProps(["title", "message", "actionName"])
</script>

<style scoped lang="scss">
    @use '../partials';


    ion-button {
        height: 3rem;
        width: 6.5625rem;
        @include partials.button-text;
        --border-radius: 7px;
    }

    ion-card {
        box-shadow: none;
    }

    ion-card-content {
        display: flex;
        padding: 1.25rem 1.5625rem;
        height: 9rem;
        column-gap: 1.25rem;
    }

    .card__icon {
        width: 1.5rem;
        height: 1.5rem;
    }
    .card__right {
            display: flex;
            flex-direction: column;
            row-gap: 1.5rem;

            &-message {
                & > h1, h4 {
                    color: #323232;
                }
                & > h1 {
                    @include partials.large-text;
                }

                & > h4 {
                    @include partials.button-text;
                    font-weight: 400;
                }
            }
        }
</style>
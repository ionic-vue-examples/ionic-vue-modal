<template>
  <ion-header>
    <ion-toolbar>
      <ion-title>Modal</ion-title>
    </ion-toolbar>
  </ion-header>
  <ion-content class="ion-padding">
    This is a modal <br />
    <ion-button @click="closeModal">Close Modal</ion-button>
  </ion-content>
</template>

<script>
import {
  IonContent,
  IonHeader,
  IonTitle,
  IonToolbar,
  IonButton,
  modalController,
} from "@ionic/vue";
import { defineComponent } from "vue";

export default defineComponent({
  name: "Modal",
  components: { IonContent, IonHeader, IonTitle, IonToolbar, IonButton },
  setup() {
    const closeModal = () => {
      modalController.dismiss();
    };

    return { closeModal };
  },
});
</script>

<template>
  <ion-page>
    <ion-header>
      <ion-toolbar>
        <ion-title>Tab 3</ion-title>
      </ion-toolbar>
    </ion-header>
    <ion-content :fullscreen="true">
      <ion-header collapse="condense">
        <ion-toolbar>
          <ion-title size="large">Tab 3</ion-title>
        </ion-toolbar>
      </ion-header>
      <button id="btn-error" @click="showError">TOMBOL BAHAYA</button>
      <ExploreContainer name="Tab 3 page" />
    </ion-content>
  </ion-page>
</template>

<style scoped>
#btn-error {
  background-color: red;
  border: none;
  color: white;
  padding: 1em 2em;
  text-align: center;
  text-decoration: none;
  display: inline-block;
  font-size: 16px;
}
</style>
<script lang="ts">
import { defineComponent } from 'vue';
import {
  IonPage,
  IonHeader,
  IonToolbar,
  IonTitle,
  IonContent,
} from '@ionic/vue';
import ExploreContainer from '@/components/ExploreContainer.vue';

export default defineComponent({
  name: 'Tab3Page',
  components: {
    ExploreContainer,
    IonHeader,
    IonToolbar,
    IonTitle,
    IonContent,
    IonPage,
  },
  setup() {
    const showError = () => {
      alert(`Error: Tombol Bahaya!`);
    };
    return {
      showError,
    };
  },
});
</script>

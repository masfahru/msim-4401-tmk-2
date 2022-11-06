<template>
  <ion-page>
    <ion-header>
      <ion-toolbar>
        <ion-title>Tab 2</ion-title>
      </ion-toolbar>
    </ion-header>
    <ion-content :fullscreen="true">
      <ion-header collapse="condense">
        <ion-toolbar>
          <ion-title size="large">Tab 2</ion-title>
        </ion-toolbar>
      </ion-header>
      <button id="btn-warn" @click="showWarning">TOMBOL PERINGATAN</button>
      <ExploreContainer name="Tab 2 page" />
    </ion-content>
  </ion-page>
</template>

<style scoped>
#btn-warn {
  background-color: orange;
  border: none;
  color: black;
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
  name: 'Tab2Page',
  components: {
    ExploreContainer,
    IonHeader,
    IonToolbar,
    IonTitle,
    IonContent,
    IonPage,
  },
  setup() {
    const showWarning = () => {
      alert(`Error: Tombol Peringatan!`);
    };
    return {
      showWarning,
    };
  },
});
</script>

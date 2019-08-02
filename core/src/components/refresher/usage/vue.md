```html
<template>
  <!-- Default Refresher -->
  <ion-4-content>
    <ion-refresher slot="fixed" @ionRefresh="doRefresh($event)">
      <ion-refresher-content></ion-refresher-content>
    </ion-refresher>
  <ion-4-content>

  <!-- Custom Refresher Properties -->
  <ion-4-content>
    <ion-refresher slot="fixed" pull-factor="0.5" pull-min="100" pull-max="200">
      <ion-refresher-content></ion-refresher-content>
    </ion-refresher>
  <ion-4-content>

  <!-- Custom Refresher Content -->
  <ion-4-content>
    <ion-refresher slot="fixed" @ionRefresh="doRefresh($event)">
      <ion-refresher-content
        pulling-icon="arrow-dropdown"
        pulling-text="Pull to refresh"
        refreshing-spinner="circles"
        refreshing-text="Refreshing...">
      </ion-refresher-content>
    </ion-refresher>
  <ion-4-content>
</template>

<script lang="ts">
  import { Component, Vue } from 'vue-property-decorator';

  @Component()
  export default class Example extends Vue {

    doRefresh(event) {
      console.log('Begin async operation');

      setTimeout(() => {
        console.log('Async operation has ended');
        event.target.complete();
      }, 2000);
    }
  }
</script>
```

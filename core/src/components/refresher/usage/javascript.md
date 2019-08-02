```html
<!-- Default Refresher -->
<ion-4-content>
  <ion-refresher slot="fixed">
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
  <ion-refresher slot="fixed">
    <ion-refresher-content
      pulling-icon="arrow-dropdown"
      pulling-text="Pull to refresh"
      refreshing-spinner="circles"
      refreshing-text="Refreshing...">
    </ion-refresher-content>
  </ion-refresher>
<ion-4-content>
```

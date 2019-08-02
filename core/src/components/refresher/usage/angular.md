```html
<!-- Default Refresher -->
<ion-4-content>
  <ion-refresher slot="fixed" (ionRefresh)="doRefresh($event)">
    <ion-refresher-content></ion-refresher-content>
  </ion-refresher>
<ion-4-content>

<!-- Custom Refresher Properties -->
<ion-4-content>
  <ion-refresher slot="fixed" pullFactor="0.5" pullMin="100" pullMax="200">
    <ion-refresher-content></ion-refresher-content>
  </ion-refresher>
<ion-4-content>

<!-- Custom Refresher Content -->
<ion-4-content>
  <ion-refresher slot="fixed" (ionRefresh)="doRefresh($event)">
    <ion-refresher-content
      pullingIcon="arrow-dropdown"
      pullingText="Pull to refresh"
      refreshingSpinner="circles"
      refreshingText="Refreshing...">
    </ion-refresher-content>
  </ion-refresher>
<ion-4-content>
```

```typescript
import { Component } from '@angular/core';

@Component({
  selector: 'refresher-example',
  templateUrl: 'refresher-example.html',
  styleUrls: ['./refresher-example.css'],
})
export class RefresherExample {
  constructor() {}

  doRefresh(event) {
    console.log('Begin async operation');

    setTimeout(() => {
      console.log('Async operation has ended');
      event.target.complete();
    }, 2000);
  }
}
```

```html
<ion-4-content><ion-4-content>
```

```javascript
var content = document.querySelector('ion-content');
content.scrollEvents = true;
content.addEventListener('ionScrollStart', () => console.log('scroll start'));
content.addEventListener('ionScroll', (ev) => console.log('scroll', ev.detail));
content.addEventListener('ionScrollEnd', () => console.log('scroll end'));
```

# Angular

## Pipes
```js
import { Pipe, PipeTransform } from '@angular/core';

@Pipe({ name: 'transform' });
export class TransformPipe implements PipeTransform {
  transform(str: string): string {
    return str.toUpperCase();
  }
}
```

## Animations
```js
// component.ts
import { trigger, state, style, animate } from '@angular/animations';

@Component({
  selector: 'animated-box',
  animations: [
    trigger('myAnimation', [
      state('preparing', style({ ...styles })),
      transition('state1 => state2', animate('0.2s ease-in')),
      transition('* <=> state2', animate('...')),
    ]),
  ],
})

// template.ts
div[@myAnimation]="state"
```

### Callbacks
```js
div(
  (@myAnimation.start)="onAnimationStart($event)"
  (@myAnimation.done)="onAnimationDone($event)"
)
```

## Routes
### Guard
```js
import { Injectable } from '@angular/core';
import { CanActivate } from '@angular/router';

Injectable()
export class MyGuard implements CanActivate {
  canActivate() {
    return true || false;
  }
}

// routes.ts
export [ { path: '/foo', canActivate: [MyGuard] } ];
```

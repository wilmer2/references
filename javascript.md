### Conditionals
```js
if (condition) {
  // ...
} else if (condition) {
  // ...
}

switch (foo) {
  case condition:

    break;
  default:

}
```

### Arrays

```js
.concat(any...): void
.entries(): Iterator
.every( mapFn, ctx?): boolean
.fill(val: any, start?: number, end?: number): any[]
.filter( mapFn, ctx?): any[]
.find( mapFn, ctx?): any // not found undefined
.findIndex(mapFn, ctx?): number // not found -1
.forEach(mapFn, ctx?): void
.includes(search: any, fromIdx?: number): boolean
.indexOf(search: any, fromIdx?: number): number // not found -1
.join(separator?: string): string
.keys(): string|number[]
.lastIndexOf(search: any, fromIdx?: number): number // not found -1
.map(mapFn2, ctx?): any[]
.pop(): any // undefined
.reduce(redFn, initVal: any): any
.reduceRight(redFn, initVal: any): any
.reverse(): any[]
.shift(): any // undefined
.slice(begin?: number, end?: number): any[]
.some(mapFn, ctx?): boolean
.sort(cmpFn): any[]
.splice(start: number, delCount: number, insertEl: any...)
.unshift(el: any...): number // undefined
.toString()
.values(): Iterator
//-- Maps --
mapFn(el: any, idx: number, arr: any[]) => boolean
mapFn2(el: any, idx: number, arr: any[]) => any
redFn(acc: any, val: any, idx: number, arr: array) => any
cmpFn(curVal: any, nextVal: any) => any
```

### Concatenative Inheritance

Object.asssign()

### Monkey Patching?
Extender el prototype de algo nativo para agregarle funcionalidad

### Prototypes
```
__proto__ == Object.getPrototypeOf
.prototype // Es para constructores es el 'objeto' que será asignado a las instancias aunque no es el prototype final
```

# Non-enumerable property for JS object

## Install

```shell
npm i @kovalenko/virtual-property
```

## Usage

```typescript
import {VirtualProperty} from '@kovalenko/virtual-property';

class MyClass {
  prop1: string;

  prop2: number;

  @VirtualProperty
  virtualProperty: string;
}

const myObj = new MyClass();
myObj.prop1 = 'foo';
myObj.prop2 = 0;

// does not enumerate
myObj.virtualProperty = 'bar';

const str = JSON.stringify(myObj); // {"prop1": "foo", "prop2": 0}
```

## License
MIT

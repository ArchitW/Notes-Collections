# Typescript (:type)

## Online Refrences (todo):
- [typescripttutorial.net](https://www.typescripttutorial.net/) - HTML


## Installation



```sh
to do
```

## Plugins (Todo)

| Plugin | info |
| ------ | ------ |
| xx | xxx  |

# Notes (Todo)
## Basic Types 
| Type | Signature | Example | Read me |
| ------ | ------ | ------ | ------ |
| **Number** | `:number`  | `let sum: number;` | int, float, +ve. -ve All numbers  |
| **String** | `:string`  | `let name: string` | String  |
| **Boolean** | `:boolean`  | `let isActive: false` | True or False  |
| **Array** | `:type[]`  | ``` name:string[], age:number[], mix: (number|string)[]``` | ['a','b'] , [1,2,3], [1,'a',3]  |
| **Touple** | `:[type,type]`  | `let skill:[number, string, number?]` | fixed elems, order important,  `?` Optional  |
| **Enums** | `enum name {constant1, constant2, ... };`  | `enum myMonths {'Jan', 'Feb', 'March'}` | index from 0, `enum myMonths {    Jan = 1, ...` will start from 1 ,`isItSummer(month: myMonths) { }` can be accessed `isItSummer(month.Jan) Or isItSummer(0)` |
| **Any** | `:any`  | `let result: any;` | don’t know its type at the time of writing  |
| **Void** | `:void`  | `function prints(msg:string):void{console.log(msg);}` | If does not have any return type  |
| **Never** | `:never`  | `function raiseError(message: string): never {throw new Error(message);}` | type that contains no values. Because of this, you cannot assign any value to a variable with a never type  |
| **Union** | `:(number|string)`  | `let result:number|string` | parameter that is either a number or a string |


## Classes
**ES5 VS TS**
```
 class Person {
    ssn;
    firstName;
    lastName;

    constructor(ssn, firstName, lastName) {
        this.ssn = ssn;
        this.firstName = firstName;
        this.lastName = lastName;
    }

    getFullName() {
        return `${this.firstName} ${this.lastName}`;
    }
}
```
**TS**
```
class Person {
    ssn: string;
    firstName: string;
    lastName: string;

    constructor(ssn: string, firstName: string, lastName: string) {
        this.ssn = ssn;
        this.firstName = firstName;
        this.lastName = lastName;
    }

    getFullName(): string {
        return `${this.firstName} ${this.lastName}`;
    }
}
```
```
let person = new Person(171280926, 'John', 'Doe');
```

**Private Variables**
```
class Message {
  private _message: string; // Private variables, we name like this
  ```
- get and set both have same name message() have public access modifier: prop can get accessed outside.
-  set() does not have return type.
- get/set depends on param passed ex: pp.message="xxxx" calls set and pp.message calls get.
```
  public get message(): string {
    return this._message;
  }
  public set message(theMessage: string) {
    this._message = theMessage;
  }
}

let pp = new Message();
pp.message = "this is Test Message";
console.log(pp.message);

```



**Temp**

| **xx** | `xxx`  | `xx` |  xxx |
| **xx** | `xxx`  | `xx` | yyy ✅ xxx ❌  |


## **<a id='Contents'>Contents</a>**

1. [Unions](#Unions)
2. [Booleans](#Booleans)
3. [Strings](#Strings)
4. [Arrays](#Arrays)
5. [Tuple](#Tuple)
6. [Enum](#Enum)
7. [Unknown](#Unknown)
8. [Any](#Any)
9. [Void](#Void)
10. [Null](#Null)
11. [Never](#Never)
12. [Object](#Object)

### **<a id='Tips'>Tips</a>**

**1. To learn the type of a variable, use typeof**

```
import axios from 'axios';
(async () => {
    const data = await axios.get('https://pokeapi.co/api/v2/pokemon/1');
console.log(data.data.species, typeof data.data.species.name);
})();
```

### Output

```
{
     name: 'bulbasaur',
     url: 'https://pokeapi.co/api/v2/pokemon-species/1/'
}
string
```

---

### **<a id='Unions'>Unions</a>**

With a union, you can declare that a type could be one of many types. For example, you can describe a boolean type as being either true or false:

`type MyBool = true | false;`

Note: If you hover over MyBool, you’ll see that it is classed as boolean. That’s a property of the Structural Type System. More on this below.

A popular use-case for union types is to describe the set of string or number literals that a value is allowed to be:

```
type WindowStates = "open" | "closed" | "minimized";
type LockStates = "locked" | "unlocked";
type PositiveOddNumbersUnderTen = 1 | 3 | 5 | 7 | 9;
```

#### [Top](#Contents)

---

### **<a id='Boolean'>Booleans</a>**

---

#### Declaration

```
let tired: boolean = true;
```

#### Usage

```
(() => {
    let tired: boolean = true;
    if(tired){
        console.log("I am tired");
    } else {
        console.log(`I'm not that tired!`)
    }
})()

```

#### [Top](#Contents)

---

### **<a id='Strings'>Strings</a>**

---

#### Declaration

```
let name: string = 'Aaron';
```

#### Usage

```
(() => {
    let name: string = 'Aaron';
    console.log(name);
})()
```

#### [Top](#Contents)

### **<a id='Arrays'>Arrays</a>**

---

#### Declaration

```
let names: string[] = ['Aaron', 'Eric'];
```

#### Usage

```
(() => {
    let names: string[] = ['Aaron', 'Eric', 'John', 'Michael'];
    console.log(names);
})()
```

- You can also use generic array types ie:

```
(() => {
    let names: Array<string> = ['Aaron', 'Eric', 'John', 'Michael'];
    console.log(names);
})()
```

#### [Top](#Contents)

---

### **<a id='Tuple'>Tuple</a>**

---

#### Declaration

```
let x: [string, string, number];
```

#### Usage

```
(() => {
    let x: [string, string, number];
    x = ["New Year", 'Sunday', 31];
    console.log(x);
})()
```

#### [Top](#Contents)

---

### **<a id='Enum'>Enum</a>**

---

#### Declaration

- An enum is a way of giving more friendly names to sets of numeric values. (numeric values will default if not implicitly set)

```
enum SaiyanLevel {
    SSJ = 1, //1
    SSJ2, //2
    SSJ3 //3
}
```

### Usage

```
(() => {
    enum SaiyanLevels {
        SSJ,
        SSJ2,
        SSJ3,
        SSJ4,
    }
    let s:SaiyanLevels = SaiyanLevels.SSJ4;
    console.log(s);
})()
```

#### Output:

```
4
```

- You are also able to print the name of a specific value of an enum.

```
(() => {
    enum SaiyanLevels {
        SSJ,
        SSJ2,
        SSJ3,
        SSJ4,
    }
    let s:string = SaiyanLevels[3];
    console.log(s);
})()
```

### Output

```
SSJ4
```

#### [Top](#Contents)

---

### <a id='Unknown'>**Unknown**</a>

---

For variables that the type is unknown

#### Declaration

```
const value: unknown = 5;
```

#### Usage

```
(() => {
  const value: unknown = 5;
  console.log(value);
})();

```

### Output

```
5
```

#### [Top](#Contents)

---

### <a id='Any'>**Any**</a>

---

#### Declaration

```
let name: any = 'Din Djarin';
```

#### Usage

```
(() => {
  let mandoParty: any = {
    leader: 'Din Djarin',
    members: ['Grogu', 'Ahsoka']
  };

  /*   None of the following lines of code will throw compiler errors.
  Using `any` disables all further type checking, and it is assumed
  you know the environment better than TypeScript. */

  mandoParty.foo(); // method does not exist, just here for example.
  mandoParty.transportation = 'ship';
  const test: number = mandoParty;
})();
```

#### [Top](#Contents)

---

### <a id='Void'>**Void**</a>

---

Void type is a function which returns `undefined` or has no return value

#### Declaration

```
const value: void = undefined;

```

#### Usage

```
(() => {
  const value: void = undefined;
  const value: void = 1; // error
  console.log(value);
})();

```

### Output

```
undefined
```

#### [Top](#Contents)

---

### <a id='Null'>**Null**</a>

---

#### Declaration

```
const value: null = null;
```

#### Usage

```
(() => {
  const value: null = null;
  console.log(value);
})();

```

### Output

```
null
```

#### [Top](#Contents)

---

### <a id='Never'>**Never**</a>

It’s not possible that this type could happen

- The never type is used when you are sure that something is never going to occur. For example, you write a function which will not return to its end point or always throws an exception.

#### Declaration

```
const neverFunc = (): never => {
  throw new Error('never');
};
```

#### [Top](#Contents)

---

### <a id='Object'>**Object**</a>

---

#### Declaration

```
let myObject: object;
myObject = {
    name: 'Luke Skywalker',
    alignment: 'Light Side'
  };

```

#### Usage

```
(() => {
  let myObject: object;

  myObject = {
    name: 'Luke Skywalker',
    alignment: 'Light Side'
  };
  console.log(myObject);
})();
```

### Note

To explicitly specify properties of the `employee` object, you first use the following syntax to declare the myObject object.

```
let myObject: {
    name: string;
    alignment: string;
    };
// then assign the myObject object to a literal object with the appropriate properties.

    myObject = {
    name: 'Luke Skywalker',
    alignment: 'Light Side'
    };

```

### Or

```
let myObject: {
    name: string;
    alignment: string;
    } = {
    name: 'Luke Skywalker',
    alignment: 'Light Side'
    };
```

#### [Top](#Contents)

---

### **[Back](./Typescript.md)**

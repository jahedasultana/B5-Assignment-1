## Differences Between Interfaces and Types in TypeScript

Interfaces and types in TypeScript are both used to define the shape of data. Interfaces are best for objects and can be extended using extends. Types can describe any kind of value, including unions and primitives. Interfaces can be merged (declared multiple times), but types cannot. Use interface when working with objects or classes, and type when you need more flexibility.

### Example
```typescript
interface Person {
  name: string;
}

type Animal = {
  name: string;
} | string;

```

## Use of the keyof Keyword in TypeScript

The keyof keyword in TypeScript is used to get all the keys of an object as a union type. It helps make code safer by checking property names. For example, if an object has keys like name and age, keyof will return "name" | "age".

### Example
```typescript
type Person = {
  name: string;
  age: number;
};

type PersonKeys = keyof Person;
// PersonKeys = "name" | "age"

```
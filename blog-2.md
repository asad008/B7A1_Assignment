# How Generics Help Build Reusable and Type-Safe Code in TypeScript

## Introduction

Generics allow developers to create reusable and type-safe code in TypeScript.

---

## Generic Function Example

```ts
function getValue<T>(value: T): T {
  return value;
}
```

This function works with multiple data types.

```ts
getValue<string>("Hello");
getValue<number>(100);
```

---

## Benefits of Generics

### Reusable Code

```ts
function createArray<T>(item: T): T[] {
  return [item];
}
```

### Strong Type Safety

```ts
const numbers = createArray<number>(10);
```

The result becomes `number[]`.

---

## Generics with Interface

```ts
interface ApiResponse<T> {
  success: boolean;
  data: T;
}
```

---

## Conclusion

Generics reduce code duplication and improve type safety in TypeScript applications.

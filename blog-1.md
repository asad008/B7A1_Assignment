# Why `any` is a Type Safety Hole and `unknown` is Safer in TypeScript

## Introduction

TypeScript provides strong type safety, but the `any` type removes those protections. Developers call `any` a “type safety hole” because it disables type checking.

The `unknown` type is a safer alternative because it forces developers to check the type before using the value.

---

## Problems with `any`

```ts
let data: any = 10;

data.toUpperCase();
```

This compiles successfully, but it crashes at runtime because numbers do not have `toUpperCase()`.

---

## Why `unknown` is Safer

```ts
let value: unknown = "TypeScript";

if (typeof value === "string") {
  console.log(value.toUpperCase());
}
```

TypeScript understands that `value` is a string inside the `if` block.

---

## Type Narrowing

Type narrowing means checking the type before using a value.

```ts
function printValue(value: unknown): void {
  if (typeof value === "number") {
    console.log(value.toFixed(2));
  }
}
```

This helps prevent runtime errors.

---

## Conclusion

The `any` type should be avoided because it removes TypeScript’s safety system. The `unknown` type is safer because it requires proper type checking before use.

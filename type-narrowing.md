# Understanding Type Narrowing in TypeScript

## Introduction
Type narrowing is the process by which TypeScript refines a broad or ambiguous type, such as a union type, into a more specific and predictable type within a conditional code block. This allows developers to safely access properties and invoke methods without triggering runtime errors.

## Core Mechanisms of Type Narrowing

### 1. The `typeof` Guard
The `typeof` operator is used to narrow down primitive data types, including `string`, `number`, `boolean`, and `symbol`.

```typescript
function formatInput(val: string | number): string {
  if (typeof val === "number") {
    return val.toFixed(2);
  }
  return val.trim();
}
```

### 2. The `in` Operator Guard
The `in` operator checks whether a specific property exists on an object, making it ideal for differentiating between distinct object shapes.

```typescript
type Member = { name: string };
type Admin = { name: string; permissions: string[] };

function handleUser(person: Member | Admin): void {
  if ("permissions" in person) {
    console.log(`Admin has ${person.permissions.length} permissions.`);
  } else {
    console.log(`Standard member: ${person.name}`);
  }
}
```

### 3. The `instanceof` Guard
When dealing with class instances and object-oriented programming, the `instanceof` operator verifies whether an object was instantiated from a specific constructor or class.

```typescript
class CustomError extends Error {
  code = 500;
}

function processError(err: Error): void {
  if (err instanceof CustomError) {
    console.error(`Custom Error Code: ${err.code}`);
  } else {
    console.error(err.message);
  }
}
```

## Conclusion
Type narrowing bridges static compile-time type safety with dynamic JavaScript runtime execution. By using `typeof`, `in`, and `instanceof`, developers can write robust, predictable code with complete confidence.


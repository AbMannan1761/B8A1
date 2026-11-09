# B8A1 - TypeScript & OOP Problem Solving

This repository contains solutions for **Assignment 1 (B8A1): Problem Solving with TypeScript & OOP** of Programming Hero Level 2 (Next Level Web Development, Batch 8).

## Overview

The assignment focuses on practical implementations of foundational and advanced TypeScript concepts, including:
- Type annotations, unions, and type inference
- Optional parameters and default behavior handling
- Readonly tuples and destructuring
- Generic functions, rest parameters, and `keyof` constraints
- Interface modeling and array operations
- Object-Oriented Programming (OOP) with access modifiers (`protected`, `private`) and inheritance (`super`)
- Asynchronous operations using `Promise` and `setTimeout`

## Repository Structure

```text
├── solutions.ts
├── type-vs-interface.md
├── type-narrowing.md
└── README.md
```

## Problem Solving (`solutions.ts`)

All 8 problem solutions are implemented in `solutions.ts` strictly adhering to the assignment requirements:
1. `multiplyValue`: Handles optional multiplier and correctly accounts for `0`.
2. `processInput`: Uses union types and `typeof` narrowing to format strings, numbers, and booleans.
3. `formatCoordinate`: Enforces a readonly tuple `[number, number, string]` and returns structured location data.
4. `concatenateArrays`: Generic function combining multiple arrays of type `T` using rest parameters.
5. `getPopularCourses`: Filters course objects adhering to the `Course` interface without mutating state.
6. `pluckValues`: Generic utility extracting property values using `<T, K extends keyof T>`.
7. `Employee` & `Manager`: Demonstrates inheritance, constructor parameter mapping, and `protected`/`private` encapsulation.
8. `validateAgeAsync`: Asynchronous age validation returning `Promise<string>` with simulated delay and rejection handling.

## Technical Blog Posts

- [Core Differences Between Type Aliases and Interfaces](type-vs-interface.md)
- [Mastering Type Narrowing in TypeScript](type-narrowing.md)

## Author

- **Student Name:** Mohammad Abdul Mannan
- **Student ID:** L2B8-0010
- **Batch:** Level 2 Batch 8 (Programming Hero)


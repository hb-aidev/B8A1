# Type vs Interface in Typescript: Core Difference and When to Use Them.

## Introduction:
Although Type and Interface in Typescript both are looking similar but they have important difference. Both help developers to describe the structure of objects and improve code readability. Both help us to define custom types.

## Core Difference:
An Interface primarily designed to define the shape of objects and support object-oriented programming. for example:

```
interface User {
  id: number;
  name: string;
}

const user: User = {
  id: 101,
  name: "Sakib"
};
```

On the other hand, type alias is more flexible to defining objects because it supports unions, intersections, primitive types, and tuples.

```
type User = {
  id: number;
  name: string;
};

type Status = "active" | "inactive";
type ID = string | number;
```

#### Interfaces can merge: 
If we declare the same interface more than once, Typescript will automatically combine them into one. Type aliases will through an error, if we use the same name twice.

#### Both can combine features:
Interface use the ``` extends ``` keyword to build on top of each other, while type alias use an intersection (``` & ```) to combine shapes.

## When We Should Choose One?
We should choose *Interface* when defining object shapes, class contracts, or public APIs that may need extension through decleartion marging.

We should choose *type* when working with unions, intersections, tuples, primitive types, or more complex type combination.

## Conclusion:
There is no universally better, both are essential feature in Typescript. Type for flexible type definations and Interface for extensible object structure. The most important is to maintain consistencey throughout the project


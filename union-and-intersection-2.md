# Combining Union (|) and Intersection (&) in Typescript

#### Introduction:
Typescript provides two useful features: Union (|) and Intersection (&) types. A Union type allows a variable to have one of multiple types. An Intersection type combines two or more types into one. We can use both together to flexible and reusable code.

#### Practical Example:
Let suppose we have two types: *Name* and *Age*. We want to create a person that contains both properties. We also want to allow a function accept either a Person or a String.

For example, first we are creating two simple types: 

```
type Name = {
    name: string;
}

type Age = {
    age: number;
}
```

Using Intersection (&) to combine them:
```
type Person = Name & Age;
```

Let's create a function that accepts both:
```
const showUser(user: User): void {
    if (typeof user === "string") {
        console.log(user);
    } else {
        console.log(user.name, user.age);
    }
}

showUser("Rakib");
showUser({ name: "Kabir", age: 25})
```

Output:
```
Rakib
Kabir 25
```

Here we can see that, Intersection (&) combines *Name* and *Age* into one *Person* type. Union (|) allows *User* to accept either a *Person* object or a string.

#### Conclusion:
*Union* and *Intersecti*on* types make TypeScript code easier to organize and reuse. We can use *Intersection* to combine properties and *Union* to allow multiple possible types.

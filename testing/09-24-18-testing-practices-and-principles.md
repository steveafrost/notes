# Testing Practices and Principles

## Resources

https://frontendmasters.com/courses/testing-practices-principles/introduction/

What kind of bugs are there

-   Memory Leaks
-   Logic
-   Integration
-   Off by 1 error
-   Raised conditions
-   Null pointer exception
-   Regression
-   Accessibility
-   User Interface
-   LOTS!

How do we prevent bugs?

-   Static Typing w/ Flow & Typescript
-   Linting w/ ESLint
-   Testing

What kinds of testing can we do?

-   Unit Testing
-   Integration
-   End to End
-   Regression
-   Acceptance
-   Performance
-   Internationalization
-   Accessibility
-   LOTS

Example of what an assertion looks like

```javascript
function expect(actual) {
    return {
        toBe(expected) {
            if (result !== expected) {
                throw new Error(`${result} is not equal to ${expected}`);
            }
        },
    };
}
```

Testing frameworks can help improve our error messaging, allow us to see exactly where something failed, and provide encapsulation.

Example of a test format

```javascript
test(title, () => {
    // arrange
    // act
    // asset
});
```

# Testing Practices and Principles

## Resources

https://frontendmasters.com/courses/testing-practices-principles/introduction/

#### What kind of bugs are there

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

#### How do we prevent bugs?

-   Static Typing w/ Flow & Typescript
-   Linting w/ ESLint
-   Testing

#### What kinds of testing can we do?

-   Unit Testing
-   Integration
-   End to End
-   Regression
-   Acceptance
-   Performance
-   Internationalization
-   Accessibility
-   LOTS

#### Example of what an assertion looks like

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

The more that your tests ressemble the way your software is used the more confidence those tests can give you

#### Confirming your assertions are running & testing code

When running assertions, check that they run. With Jest you can use expect.assertions(num) where num is the amount of assertions you expect to run. The better way is to break the source code it is testing. That way you both find out that the assertions are indeed running and that it is indeed testing the code you think it is testing.

That's why writing tests first, or TDD, is more useful because your tests fail intially so you know the assertions are running and then as you write the code to pass that test, you'll see the assertions succeed.

It's best to have one assertion per test unless you are using a framework w/ good errors messages which can locate which assertion in the test failed.

### Assertions

-   `toBe`
    -   Tests like `===` would so {} _does not_ equal {}
-   `toEqual`
    -   Tests if something looks like something else so {} _does_ equal {}
-   `toMatchObject`
    -   First object has at least as much as second object has including nesting
-   etc

### Mock Functions

Functions that keep track of how their called and what they're called with

Looks like `const myFn = jest.fn()` and has methods on it like `.mock` and `.mock.calls` which can keep track of it's history.

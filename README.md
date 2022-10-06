## React Conference

### Workshop:1 Comprehensive guide to testing React applications

https://github.com/krambertech/react-testing-workshop
- [ ] userEvent over fireEvent
- [ ] Priority of selector
- [ ] Regex for matcher (more high-level, not case sensitive etc…)
- [ ] userEvent.type(passwordInput, "password{enter}"); — look at the enter
- [ ] toHaveTextContent ( used often)
- [ ] Multiple options for async operation
    - [ ] waitForElementToBeRemoved then expect with getBy*  (Speaker use this more often)
    - [ ] findBy*
    - [ ] await waitFor(() => expect(mockLogin).toBeCalledTimes(1))
- [ ] Act warning => 
- [ ] Not recommended to mock custom hook - rather you mock underlying api response ( may be through service worker)
- [ ] Accessibility in chrome debugger to check role value

### Workshop:2 Typescript for react developer
- [ ] Runtime type validation (generally we write type definitions to match what we expect but generally its not gurrentee, been only able to find out when code broke at runtime - sometimes hard to debug. hence runtime type validation comes to rescue -- Speaker demoed it with funtypes and funtypes-schemas, but there are other options available (i.e: joi) 
- [ ] ts-expect-error vs ts-ignore-error. (Recommended to use ts-expect-error bcz it will scream if its not an error anymore)


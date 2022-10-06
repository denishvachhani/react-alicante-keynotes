## React Conference 💻 🌞 🏖️ 🇪🇸

Disclaimer: Below are my interpretations/notes/learnings from all talks/sessions, these may NOT be 100% right :)

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

Exercises and guide: https://github.com/denishvachhani/react-alicante-keynotes/blob/main/typescript-for-react-developers.pdf

- [ ] Runtime type validation (generally we write type definitions to match what we expect but generally its not gurrentee, been only able to find out when code broke at runtime - sometimes hard to debug. hence runtime type validation comes to rescue -- Speaker demoed it with funtypes and funtypes-schemas, but there are other options available (i.e: joi) 
- [ ] ts-expect-error vs ts-ignore-error. (Recommended to use ts-expect-error bcz it will scream if its not an error anymore)
- [ ] types vs interface (interface is better for typing comprehensive object types as it give better info in error popup)

### useEffect – Managing Effects More Effectively 
- [ ] useEffect is not for all effects
- [ ] useEffect is not a lifecycle hook
- [ ] Default behaviour of useEffect is infinite loop
- [ ] useEffect is really should be used for  synchronisation and not to perform side effect.
- [ ] But where do side effects go then??
- [ ] Event handlers is one answer —> ie. onClick, onSubmit 
- [ ] useEffect —> eventHandler()
- [ ] eventHandler —> onSubmit —> send (‘’) — you could perform logic there
- [ ] Stately.ai/editor
- [ ] You don’t need useEffect for fetching data —> renderAsYouNeed (Remix, ReactQuery, useSwr etc…)

### GraphQl 
- [ ] More empathises on graphQl
- [ ] Query language for API ( not a framework)
- [ ] Type in build
- [ ] Always send post request 
- [ ] Use GraphQl schema as source of truth
- [ ] Use codegen — it auto generate typescript types from graphQL schema - so client don’t have to duplicate it.
- [ ] GraphQl and Typescript - made for each other

### React Remixed
- [ ] Remix automatically handles errors, interruptions and race conditions
- [ ] Remix build times are nearly instant and decoupled from data
- [ ] Nested routing, 
- [ ] Underlying web apis
- [ ] Remix is like an Angular (inbuilt data fetching, routing etc….)

### Button vs Link
- [ ] Don't mix the usages of each for betterment of accessiblity and UX
- [ ] Technically you could just style Link -> Button and Button -> Link -- Don't.

### Cross platform design system architecture (React and React Native)
- [ ] Way 1 : separate team for each but cons are more ( and expensive)
- [ ] Way 2: React-native-web
- [ ] Same code works in react and react-native
    - [ ] Step1: abstract styles
    - [ ] Step2: import { TextInput } from ‘design-system’
    - [ ] Web pack resolve file name 
        - [ ] Text.web.tsx
        - [ ] Text.native.tsx
    - [ ] Jest to configure
    - [ ] Rollup to bundle two separate build as well as type (one type for both web and native as original purpose is to have same API)
    - [ ] What about accessibility ? (  )
    - [ ] Platform dependent property - marked as optional in Type script and also add error while trying to use
    - [ ] Platform dependent types














# React FAQ

## Description

Helpful collection of common questions and clear answers about React ecosystem.

## Table of Contents

- [How to create new project?](#how-to-create-new-project?)
- [Why am I seeing two messages for one console.log?](#why-am-I-seeing-two-messages-for-one-console.log?)

### How to create new project?

To create a new React project quickly and efficiently, you can use [Vite](https://vitejs.dev/). While the latest React documentation encourages using frameworks like Next.js or Remix for advanced features, these are not required. Vite is ideal for simpler setups, offering speed and flexibility. It's also important to note that Create React App (CRA) is no longer [maintained](https://github.com/reactjs/react.dev/pull/5487#issuecomment-1409720741), making Vite a more modern and supported choice for starting new React projects.

```bash
npm create vite@latest
```

### Why am I seeing two messages for one console.log?

If you're seeing two messages from a single console.log, your code might look like this:

```jsx
...
useEffect(() => {
  console.log("effect");
}, []);
...
```

or

```jsx
export function Button(props){
  ...
  console.log("render");
  ...
}
```

This happens because of React's [Strict mode](https://react.dev/reference/react/StrictMode#strictmode), which is enabled by default in new React apps. Strict Mode intentionally calls some functions twice during development to help you spot side effects and other potential issues.

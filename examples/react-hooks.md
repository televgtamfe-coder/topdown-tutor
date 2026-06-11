# React Hooks

## Overall Picture

React Hooks are a way to let function components use state, side effects, and shared React features without switching to class components.

## Distinctive Features

- They keep stateful logic inside functions.
- They make reusable logic easier through custom hooks.
- They must follow strict calling rules.

## Internal Logic

Hooks let React match calls by order, so the component must call them consistently on every render.

## Top 10 Knowledge Points

1. `useState` stores local state.
2. `useEffect` handles side effects.
3. `useRef` stores a mutable value that survives renders.
4. Hooks must be called at the top level.
5. Hooks must not be called conditionally.
6. Custom hooks package reusable logic.
7. Effects run after render.
8. Dependency arrays control re-running behavior.
9. Cleanup prevents leaks and stale subscriptions.
10. Hook rules matter because React tracks them by call order.

## Key Checks

1. Why can hooks not be called conditionally?
2. What problem does `useEffect` solve?
3. What is the difference between `useState` and `useRef`?

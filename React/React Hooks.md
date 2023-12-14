As of my last knowledge update in January 2022, React has several built-in hooks, each serving a specific purpose. However, it's worth noting that React evolves, and new features may have been introduced since then. Here's a list of the core React hooks available as of my last update:

1. **useState:** Used to add state to functional components.

   ```jsx
   const [state, setState] = useState(initialState);
   ```

2. **useEffect:** Enables side effects in functional components, such as data fetching or DOM manipulation.

   ```jsx
   useEffect(() => {
     // Side effect code
     return () => {
       // Cleanup code (optional)
     };
   }, [dependencies]);
   ```

3. **useContext:** Allows functional components to subscribe to a context without introducing nesting.

   ```jsx
   const value = useContext(MyContext);
   ```

4. **useReducer:** An alternative to `useState` for managing more complex state logic.

   ```jsx
   const [state, dispatch] = useReducer(reducer, initialState);
   ```

5. **useCallback:** Memoizes a callback function to prevent unnecessary re-renders in child components.

   ```jsx
   const memoizedCallback = useCallback(() => {
     // Callback code
   }, [dependencies]);
   ```

6. **useMemo:** Memoizes a value to optimize performance by preventing unnecessary calculations.

   ```jsx
   const memoizedValue = useMemo(() => computeExpensiveValue(a, b), [a, b]);
   ```

7. **useRef:** Creates a mutable object that persists across renders and doesn't cause re-renders when changed.

   ```jsx
   const myRef = useRef(initialValue);
   ```

8. **useImperativeHandle:** Customizes the instance value that is exposed when using `React.forwardRef`.

   ```jsx
   useImperativeHandle(ref, () => ({
     // Custom instance value
   }), [dependencies]);
   ```

9. **useLayoutEffect:** Similar to `useEffect`, but fires synchronously after all DOM mutations.

   ```jsx
   useLayoutEffect(() => {
     // Effect code
   }, [dependencies]);
   ```

10. **useDebugValue:** Displays a label for custom hooks in React DevTools.

    ```jsx
    useDebugValue(value);
    ```

Remember to check the official React documentation for the latest information on hooks and any additional hooks that may have been introduced in newer versions of React.
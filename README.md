# layout.tsx `params` is not a valid object/prop using Parallel Routes & Intercepting Routes

## Steps to reproduce

1. `npm install`
2. `npm run dev`
3. Go to `http://localhost:3000/en` (Locale is important)
4. See error in console:

   ```
   Warning: React.createElement: type is invalid -- expected a string (for built-in components) or a class/function (for composite components) but got: undefined. You likely forgot to export your component from the file it's defined in, or you might have mixed up default and named imports.

   ⨯ src/app/[locale]/layout.tsx (19:25) @ locale
   ⨯ TypeError: Cannot read properties of undefined (reading 'locale')
       at RootLayout (./src/app/[locale]/layout.tsx:20:94)
       at stringify (<anonymous>)
    17 |   console.log({
     18 |     /* This will throw an error that it's not a valid element... */
   > 19 |     locale: props.params.locale,
        |                         ^
    20 |   });
    21 |
    22 |   return (
   ```

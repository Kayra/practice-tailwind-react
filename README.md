# pratice-tailwind-react

Using [Sebastian's tutorial](https://medium.com/codingthesmartway-com-blog/how-to-use-tailwind-css-with-react-9dd78bbdc0e0)

## Start a Tailwind React project

Create the initial React project:

```bash
npx create-react-app example-tailwind-react-app
```

Install Tailwind and it's dependencies (**in the newly generated react app directory**):

```bash
npm install -D tailwindcss postcss autoprefixer
```

Generate the Tailwind configuration files (**in the newly generated react app directory**):

```bash
npx tailwindcss init -p
```

Update the newly created `tailwind.config.js` file with the path to the desired react template files:

```js
module.exports = {
   content: [
     "./src/**/*.{js,jsx,ts,tsx}",
   ],
   theme: {
     extend: {},
   },
   plugins: [],
 }
```

Update the `index.css` file with the Tailwind CSS directives:

```css
@tailwind base;
@tailwind components;
@tailwind utilities;
```

Update the default code in `src/App.js` with example code using Tailwind CSS classes:

```jsx
function App() {
  return (
    <div className="container mx-auto bg-gray-200 rounded-xl shadow border p-8 m-10">
      <p className="text-3xl text-gray-700 font-bold mb-5">
        Welcome!
      </p>
      <p className="text-gray-500 text-lg">
        React and Tailwind CSS in action
      </p>
    </div>
  );
}
export default App;
```

Run the server to see Tailwind in action:

```bash
npm run start
```

## Useful Commands

Generate a Tailwind build:

```bash
npx tailwindcss -o ./css/styles.min.css --minify
```

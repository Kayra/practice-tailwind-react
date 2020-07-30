# pratice-tailwind-react

A short introduction into setting up and using Tailwind with React pulled mostly from the [Tailwind docs](https://tailwindcss.com/docs/guides/create-react-app). (I made this before using it for my [spotify-tools](https://github.com/Kayra/spotify-tools) project). 

[Tailwind](https://tailwindcss.com/) is a CSS framework and [React](https://reactjs.org/) is a framework used to build user interfaces in the browser.

Technologies used:

- node: v18.9.0
- npm/npx : 8.19.1

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
        It works!
      </p>
      <p className="text-gray-500 text-lg">
        React and Tailwind CSS are now operational.
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


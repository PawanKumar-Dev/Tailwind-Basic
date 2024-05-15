1. First we create a package.json file with running command. This create package.json without asking any    question from you.
   npm init -y

2. Next we install Tailwind CSS using npm. Here is the link:
   https://tailwindcss.com/docs/installation

3. First run this cmd. (-D stands for dev dependency)
   npm install -D tailwindcss

4. Next cmd crete config js file for Tailwind CSS
   npx tailwindcss init

5. If we want Tailwind to moniter only our HTML for changes. We modify tailwind.config.js
   /** @type {import('tailwindcss').Config} */
   module.exports = {
   content: ["*html"],
   theme: {
      extend: {},
   },
   plugins: [],
   }


6. Next we create a CSS for taking input from Tailwind CSS. Paste this code their.
   @tailwind base;
   @tailwind components;
   @tailwind utilities;

7. Next we can run a simple cmd or set a script code in our package.json to save our time. "test" is the default script in package.json so ignore it.

   "scripts": {
      "test": "echo \"Error: no test specified\" && exit 1",
      "build": "npx tailwindcss -i ./css/input.css -o ./css/output.css --watch"
   },

8. To make it easier to code install vs code extension: Tailwind CSS IntelliSense

9. Now to compile our code into Tailwind CSS we run cmd in terminal.
   npm run build

10. Don't forget to link output.css to your html file
   <link rel="stylesheet" href="css/output.css">

11. You can use Material fonts from Google fonts for free:
   <link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Material+Symbols+Outlined:opsz,wght,FILL,GRAD@24,400,0,0" />
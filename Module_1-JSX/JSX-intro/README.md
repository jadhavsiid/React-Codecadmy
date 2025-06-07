# Intro to JSX

## Why React?
- React.js is a JavaScript library developed by engineers at Facebook. 
- Significance of React:

- **React is fast**. Apps made in React can handle complex updates and still feel quick and responsive.

- **React is modular**. Instead of writing large, dense files of code, you can write many smaller, reusable files. React’s modularity can be a beautiful solution to JavaScript’s maintainability problems.

- **React is scalable**. Large programs that display a lot of changing data are where React performs best.

- **React is flexible**. You can use React for interesting projects that have nothing to do with making a web app. People are still figuring out React’s potential. There’s room to explore.

- **React is popular**. While this reason has admittedly little to do with React’s quality, the truth is that understanding React will make you more employable.


## What is JSX ?
- JSX is a syntax extension for JavaScript. It was written to be used with React. JSX code looks a lot like HTML.
  **What does “syntax extension” mean?**
  - In this case, it means that **JSX is not valid JavaScript. Web browsers can’t read it!**
  - If a JavaScript file contains JSX code, then that file will have to be compiled. This means that before the file reaches a web browser, a JSX compiler will translate any JSX into regular JavaScript.

## JSX Element
- A basic unit of JSX is called a JSX element.
- Here’s an example of a JSX element:
``` jsx

<h1>Hello world</h1>

```
- This JSX element looks exactly like HTML! The only noticeable difference is that you would find it in a JavaScript file, instead of in an HTML file.

## JSX Elements And Their Surroundings
- JSX elements are treated as JavaScript expressions. They can go anywhere that JavaScript expressions can go. This means that a JSX element can be saved in a variable, passed to a function, stored in an object or array… you name it.
- Here’s an example of a JSX element being saved in a variable:
  ``` jsx

  const navBar = <nav>I am a nav bar</nav>;

  ```
- Here’s an example of several JSX elements being stored in an object:

  ``` jsx

       const myTeam = {
       center: <li>Benzo Walli</li>,
       powerForward: <li>Rasha Loa</li>,
       smallForward: <li>Tayshaun Dasmoto</li>,
       shootingGuard: <li>Colmar Cumberbatch</li>,
       pointGuard: <li>Femi Billon</li>
     };

  ```

## Attributes In JSX
- Here are some JSX elements with attributes:
  ``` jsx

    <a href='http://www.example.com'>Welcome to the Web</a>;
    const title = <h1 id='title'>Introduction to React.js: Part I</h1>; 

  ```
- A single JSX element can have many attributes, just like in HTML:
  ```jsx

     const panda = <img src='images/panda.jpg' alt='panda' width='500px' height='500px'>;
 
  ```

## Nested JSX
- Here’s an example of a JSX <h1> element, nested inside of a JSX <a> element:
- ``` jsx
 
    <a href="https://www.example.com"><h1>Click me!</h1></a>

  ```
- To make this more readable, you can use HTML-style line breaks and indentation:
  ``` jsx

     <a href="https://www.example.com">
       <h1>
          Click me!
       </h1>
     </a>

  ```
- If a JSX expression takes up more than one line, then you must wrap the multi-line JSX expression in parentheses:

  ``` jsx
    
        (
      <a href="https://www.example.com">
        <h1>
          Click me!
        </h1>
      </a>
    )

  ```

- Nested JSX expressions can be saved as variables, passed to functions, etc., just like non-nested JSX expressions can! Here’s an example of a nested JSX expression being saved as a variable:

  ``` jsx
    
      const theExample = (
      <a href="https://www.example.com">
        <h1>
          Click me!
        </h1>
      </a>
    )

  ```

## JSX Outer Elements
- There’s a rule that we haven’t mentioned: a JSX expression must have exactly one outermost element.
- In other words, this code will work:
   
   ``` jsx
    
      const theExample = (
      <a href="https://www.example.com">
        <h1>
          Click me!
        </h1>
      </a>
    )

   ```
- But this code will not work:

    ``` jsx
    
        const paragraphs = (
        <p>I am a paragraph.</p> 
        <p>I, too, am a paragraph.</p>
    );

    ```
-**The first opening tag and the final closing tag of a JSX expression must belong to the same JSX element!**
- It’s easy to forget about this rule and end up with errors that are tough to diagnose.
- If you notice that a JSX expression has multiple outer elements, the solution is usually simple: wrap the JSX expression in a <div> element.

## JSX Rendering
- You’ve learned how to write JSX elements! Now it’s time to learn how to render them.
- **To render a JSX expression means to make it appear on screen.**
- The following code will render a JSX expression:

      ``` jsx
    
     const container = document.getElementById('app');
     const root = createRoot(container);
     root.render(<h1>Hello world</h1>);

      ```


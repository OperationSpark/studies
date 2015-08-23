# Studies

**Table of Contents**

- [Studies](#studies)
  - [Overview](#overview)
  - [Setup](#setup)
  - [Create a JSBin per JavaScript Subtopic](#create-a-jsbin-per-javascript-subtopic)
  - [Embed the Gist in your Studies](#embed-the-gist-in-your-studies)
  - [JavaScript SubTopics](#javascript-subtopics)

## Overview

You are working hard to become a kick-ass software engineer.  One of the best ways to freeze-dry your knowledge is to codify your new knowledge in study notes that include explained code examples.  By cleary recording your notes, you'll be reiterating and strengthening your working understanding of the concepts, you'll be exemplifying your comprehension to prospective employers, helping other students to learn as they walk in your footsteps, and you'll be able to return to each topic for a refresher at any time.

## Setup

1. In your Cloud9 workspace for your website project, in the **ROOT directory of your website project**, create a file called:
    studies.html
2. Open the studies.html file to edit it and insert teh following markdown:

  ````HTML
  <!DOCTYPE html>
  <html>
      <head>
          <script src="https://ajax.googleapis.com/ajax/libs/jquery/2.1.4/jquery.min.js"></script>
          <script src="https://cdnjs.cloudflare.com/ajax/libs/gist-embed/2.2/gist-embed.min.js"></script>
          <link rel="stylesheet" href="css/studies.css" type="text/css" />
          <title>Studies</title>
      </head>
      <body>
          <div id="all-contents">
          <nav>
              <header>Sheba's Glorious Website</header>
              <ul>
                  <li><a href="index.html">Home</a></li>
                  <li><a href="portfolio.html">Portfolio</a></li>
                  <li><a href="studies.html">Studies</a></li>
              </ul>
          </nav>
          <main>
              <div class="content">
                  <h1>Javascript</h1>
                  <!-- YOUR NOTE SECTIONS GO BELOW HERE -->
                  
                  
                  <!-- YOUR NOTE SECTIONS GO ABOVE HERE -->
              </div>
          </main>
      </div>
      </body>
  </html>
  ````

  **NOTE:** In the above markdown, we're loading <a href="jquery.com" target="_blank">jQuery</a> and the <a href="https://github.com/blairvanderhoof/gist-embed" target="_blank">Gist Embed</a> library - these libraries will allow us to embed into our `studies.html` page, our GitHub gists containing our code examples for our studies notes.  You can read more about those libraries at the links provided.
    
3. We are already linking to a custom CSS file, so we need to create this file.  If your website workspace does not already have a `css` directory, create one now in the ROOT directory of your website.  Into this `css` directory, create a file called `studies.css`.  Open this `studies.css` file and into paste the following CSS rules:

  ````CSS
  body {
      background: rgb(125, 198, 205);
      color: rgb(45, 45, 45);
      padding: 10px;
      font-family: arial;
  }
  
  header {
      font-size: 1.5em;
      font-weight: bold;
  }
  
  [id=all-contents] {
      max-width: 800px;
      margin: auto;
  }
  
  
  /* Main navigation menu */
  
  nav {
      background: rgb(239, 80, 41);
      margin: 0 auto;
      display: flex;
      padding: 10px;
  }
  
  nav header {
      display: flex;
      align-items: center;
      color: rgb(255, 255, 255);
      flex: 1;
  }
  
  nav ul {
      list-style-image: none;
  }
  
  nav li {
      display: inline-block;
      padding: 0 10px;
  }
  
  nav a {
      text-decoration: none;
      color: #fff;
  }
  
  
  /* Main container area beneath menu */
  
  main {
      background: rgb(245, 238, 219);
      display: flex;
      flex-direction: column;
  }
  
  [class=sidebar] {
      margin-right: 25px;
      padding: 10px;
  }
  
  [class=sidebar] img {
      width: 200px;
  }
  
  [class=content] {
      flex: 1;
      padding: 15px;
  }
  
  .content h1, h2, h3, h4, h5, h6 {
      margin: 10px;
  }
  
  .content section > a {
      text-decoration: none;
  }
  ````

  **NOTE:** These CSS rules contain the default styles from hte `first-website` project, so if you've pimped-out your styles to your liking, you'll need to edit these CSS style rules to match your fancypants styles.
    
4. Fantastic!  But now we need to link our `studies.html` page in the nav-bar of each page in our website, otherwise, our users will not be able to navigate to our `studies.html` and see how smart we are:  Open both the **ROOT** `index.html` file of your website, and the `portfolio.html` file, and edit the `<nav></nav>` of each page to it matches this (note the inclusion of the new studies `<li></li>`):

  ````HTML
          <nav>
              <header>Sheba's Glorious Website</header>
              <ul>
                  <li><a href="index.html">Home</a></li>
                  <li><a href="portfolio.html">Portfolio</a></li>
                  <li><a href="studies.html">Studies</a></li>
              </ul>
          </nav>
  ````

5. Save all your pages, and if your Apache webserver is running, you should be able to see a **Studies** link in your nav-bar, and you should be able to navigate to the `studies.html` page from each page in your website.

## Create a JSBin per JavaScript Subtopic

1. Login to JSBin via GitHub.
2. Create a new JSBin, and select **File > Add description**, and give your JSBin a description and `<title>` to match the name of the subtopic you're exemplifying, for example, "Variables".
3. Implement your JSBin to illustrate the various concepts of the JavaScript subtopic you're exemplifying.  You should have code examples that clearly show you understand the concept.  Use single-line or multiline comments to explain your code.  **Ensure your code works and is valid** by running your JSBin!

  ````javascript
  /*
   * VARIABLES:
   *
   * 0. To hold things in memory during the life-cycle of a program, we can use variables.  Variables 
   * are named identifiers that can point to values of a particular type, like a Number, String, 
   * Boolean, Array, Object or another data-type.  Variables are called so because once created, we 
   * can CHANGE the value (and type of value) to which they point.
   *
   * 1. To create a variable we use the keyword, var, followed by a name (id or alias) for our 
   * variable.
   *
   * 2. There are 2 phases of using variables: declaration and initialization (or assignment).
   */
  
  // 1. declaration //
  var myName; 
  
  /*
   * At the declaration phase, the variable myName is undefined because we have NOT initialized 
   * it to anything 
   */ 
  console.log(myName); // prints => undefined
  
  // 2. initialization or assignment //
  myName = 'john';
  console.log(myName); // prints => john
  
  // 3. re-assignment //
  myName = 'bob';
  console.log(myName); // prints => bob
  
  // NOTE: We can assign and re-assign anything to a variable - we cannot do this with constants //
  var myVariable = 1;
  var myVariable = true;
  myVariable = "someString";
  ````

4. Once you're cool with your code and you're sure it works, you want to create a **GitHub Gist** of your JSBin.  In JSBin, select **File > Export as gist**.  This will create an anonymous gist - and in the top of JSBin, click on the yellow tab at the top of the page that says, "Gist created! Open in new tab".  This will bring you to the anonymous gist at GitHub.
5. Next, **YOU MUST FORK** this anonymous gist so that it is paired with your own GitHub account.  Do this by clicking the "Fork" button in top-right corner.
6. Once you've forked your gist, you can optionally delete unused sub-files of the gist: JSBin will create separate gist files for the `html` portion of the gist, which in this case, are not needed - you are only interested in the `.js` sub-file in the gist, it will be called something like `jsbin.jihure.js`, where `jihure` is the JSBin id for your bin.  You've created your gist, pat yourself on the back, smoke'em if you got'em!

## Embed the Gist in your Studies

1. Back in your `studies.html` page, find the **content** `<div></div>` tag that looks like this:

  ````HTML
              <div class="content">
                  <h1>Javascript</h1>
                  <!-- YOUR NOTE SECTIONS GO BELOW HERE -->
                  
                  
                  <!-- YOUR NOTE SECTIONS GO ABOVE HERE -->
              </div>
  ````

    ...and between the comments that read `YOUR NOTE SECTIONS GO BELOW HERE` and `YOUR NOTE SECTIONS GO ABOVE HERE`, and per study note (gist), paste in the following `<section></section>`, this one exemplifying **Variables**:
    
  ````HTML
                  <section>
                      <hr>
                      <a href="#variables"><h2>Variables</h2></a>
                      <code data-gist-id="4ae6dead16cdb2271041" data-gist-file="jsbin.jihure.js" data-gist-hide-footer="true"></code>
                  </section>
  ````

2. Importantly, in the `<code></code>` tag, replace the `data-gist-id` attribute with your gist id (the id can be found back on your GitHub gist page, as the last number in the URL of the gist), for example, `https://gist.github.com/jfraboni/4ae6dead16cdb2271041` - the gist id here is, `4ae6dead16cdb2271041`
3. Finally, also in the `<code></code>`, replace the `data-gist-file` with the name of the gist sub-file, which you can find on the GitHub gist page, within the header of the of the JavaScript gist sub-file.  For example, the sub-file embedded from the gist at <a href="`https://gist.github.com/jfraboni/4ae6dead16cdb2271041`" target="_blank">https://gist.github.com/jfraboni/4ae6dead16cdb2271041</a> is `jsbin.jihure.js`.
4. Okay, once you do this, save your changes, then flip back to your `studies.html` page and refresh, you should see your nice section header for the subtop, plus your gist right below this, exemplifying your smartness!

## JavaScript SubTopics

1. Ensure you have JavaScript subtops exemplifying the following:
    1. Variables
    2. Datatypes (Simple & Complex):
        1. Number
        2. String
        3. Boolean
        4. Array
        5. Object
        6. Function
        7. undefined
        8. null
        9. NaN
        10. Google Infinity and -Infinity
    3. Operators:
        1. Assignment
        2. Arithmetic
        3. Comparison
        4. Logical
        5. Binary (!, typeOf, -)
        6. Turnary (a ? b : c)
    4. String manipulation
    5. Control flow: if, else-if, else
    6. Loops: while, for, for-in
        1. Be able to loop any number of times, forward counting up to some limit, backward counting down to 0
        2. Loop over an Array, forwards and backwards
        3. Loop over an Object, forwards and backwards ( hint: `keys = Object.keys(myObject);` )
    7. Functions: programs within programs!
        1. The two phases to using functions: First we must ___? Next we can execute (or two other words for executing a function?) a function by?
        2. What’s the difference between a function’s parameters and arguments PASSED to a function?
        3. What’s the syntax for a NAMED function?
        4. How do we assign a function to a variable?
        5. Functions can OPTIONALLY take inputs and OPTIONALLY return a single value, how do we specify inputs, and how do we return a value?
        6. NOTE: Primitive (simple) values are passed to a function BY COPY, complex by reference.  Try it!
        7. Scope: Functions can see and modify variables in parent or global scopes.  The inverse is NOT true.
        8. Closures: Functions form closures around the data they house.  If an object returned from the Function and is held in memory somewhere (referenced), that closure stays ALIVE, and data can continue to exist in these closures! (See: our meeting-room app for an example!) (ALSO, see: <a href="understand-javascript-closures-with-ease" target="_blank">Understanding JavaScript Closures with Ease)


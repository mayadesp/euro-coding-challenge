![Ironhack](https://s3-eu-west-1.amazonaws.com/ih-materials/uploads/upload_6e171edc323b4df30ae1f1cefe63c7e2.png)

Euro Coding Challenge: Speaker Notes
====================================
The goal is to **live-code a landing page** while attendees follow along.

**Topics to be covered:**

- HTML basic syntax
- HTML document structure
- HTML linking other documents (images & CSS)
- HTML basic tags (h1-h6, img, p, a, ul, li, etc.)
- CSS basic syntax
- CSS tag & class selectors
- CSS font & color properties
- CSS background image properties
- CSS box model properties
- CSS flexbox (layout & centering)
- Linking Google Fonts



Preparation (before workshop)
-----------------------------
Find a **second screen** to open this document or **print it**.

Open Links:
- [Slides for introduction](https://docs.google.com/presentation/d/1w-YOJCdYyiILkKwkdbwwdAROUnagCci6Vh1d9gi6Brw/edit?usp=sharing)
- [Attendee info page link](http://bit.ly/eurocoding) - For downloading images and copy/pasting pieces easily.
- [CSS Tricks' Guide to Flexbox](https://css-tricks.com/snippets/css/a-guide-to-flexbox/)
  \- For diagrams about Flexbox concepts.



Workshop
--------
### Part #1: Introduction ###
Help them get their editor and browser set up with our code files.

- **Slides** - Go through the introduction slides until it says **CODING TIME**.
- **Editor Setup** - Walk them through the setup of creating a folder for the
  project and opening that folder in the editor.
- **Directory Structure** - Teach them how to create the directory structure:
  * `index.html` file
  * `css/` folder
  * `style.css` file inside the `css/` folder
  * `images/` folder
- **Hello, world!** - Open the `index.html` file and have them type "Hello, world!".
  Teach them about **saving their files**.
- **Open `index.html`** - Show them how to see "Hello world!" in the browser.
- **Keyboard shortcuts** - Teach them save (`CMD/CTRL + S`)
  and refresh (`CMD/CTRL + R`) keyboard shortcuts.


### Part #2: HTML ###
Add the HTML piece by piece and explain any tags that are new.
They will be able to **copy/paste all the text** from their attendee info page.

- **`<!doctype html>`** - tells browsers we are using the most recent HTML.
- **`<html>`** - contains all our content. **New Concept**: tags "open" and "close".
- **`<head>`** - invisible content: title, metadata, seo, etc.
- **`<body>`** - visible content.
- **`<title>`** - tab title
- **`<meta charset="utf-8">`** - support extra characters. **New Concept**: attributes (special keywords in the tag).
- **`<h1>`** - wrap it around the "Hello, world!" and demonstrate `<h1>-<h6>`. **New Concept**: some tags to have default styling.
- **`<header>`** - above `<h1>`. **New Concept**: semantics (each tag has a meaning).
  * **`<img>`** - download `spotify-logo.png` into `images/` and link it to an `<img>` tag. **New Concept**: void tags (no close).
  ```html
  <img src="./images/spotify-logo.png" />
  ```
  * **`<nav>`** - our navigation where all the links will go.
    - **`<a>`** - `href` is for deciding where the link goes. we won't get that far.
      ```html
      <a href="#0">Premium</a>
      <a href="#0">Discover</a>
      <a href="#0">Help</a>
      <a href="#0">Download</a>
      ```
- **`<section class="big-section">`** - for other major sections of the page. **New Concept**: classes (used to distinguish tags).
  * **`<div>`** - no semantic meaning. we will need it later for CSS.
    - **`<h1>`** - put our `<h1>` in the `<div>` and add real copy: "Music for everyone."
    - **`<p>`** - for paragraphs of longer text. Copy: "Spotify is now free on mobile, tablet and computer. Listen to the right music, wherever you are."
      * **`<br>`** - for breaking lines. put it between the two sentences.
- **`<section class="features">`** - three icons section
  * **`<h2>`** - less prominent title. Copy: "What's on Spotify?"
  * **`<ul>`** - container for lists. contrast with `<ol>`.
    - **`<li>`** - item for lists. each one has more info inside. download icon images into `images/`.
      ```html
      <li>
        <img src="./images/icon-sound.png" />
        <h3>Millions of Songs</h3>
        <p>There are millions of songs on Spotify.</p>
      </li>

      <li>
        <img src="./images/icon-waveform.png" />
        <h3>HD Music</h3>
        <p>Listen to music as if you were listening live.</p>
      </li>

      <li>
        <img src="./images/icon-devices.png" />
        <h3>Stream Everywhere</h3>
        <p>Stream music on your smartphone, tablet, or computer.</p>
      </li>
      ```
- **`<section class="kanye">`** - Kanye section
  * **`<div>`** - again, we will need it later for CSS.
  * **`<img>`** - place image first since `<div>` will have a lot of stuff in it. download `kanye.jpg` into `images/`.
    ```html
    <img src="./images/kanye.jpg" />
    ```
  * **INSIDE `<div>`**:
    - **`<h2>`** - Copy: "It's as yeezy as Kanye West."
    - **`<ul>`** - another list of features.
      *  **`<li>`** - more info inside each item again.
        ```html
        <li>
          <h3>Search</h3>
          <p>
            Know what you want to listen to?
            Just search and hit play.
          </p>
        </li>

        <li>
          <h3>Browse</h3>
          <p>
            Check out the latest charts,
            brand new releases and great
            playlists for right now.
          </p>
        </li>

        <li>
          <h3>Discover</h3>
          <p>
            Enjoy new music every Monday with your own personal playlist.
            Or sit back and enjoy Radio.
          </p>
        </li>
        ```

**HTML done!**


### Part #3: CSS ###
Add the CSS piece by piece and explain new properties.
For Flexbox, show diagrams from the
[CSS Tricks' Guide to Flexbox](https://css-tricks.com/snippets/css/a-guide-to-flexbox/).

#### General CSS ####
- **`<link>`** - connects our CSS code file to our HTML document. also add the Google Fonts link while we are at it (in the attendee info page).
  ```html
  <link href="https://fonts.googleapis.com/css?family=Open+Sans:300,400" rel="stylesheet">
  <link rel="stylesheet" href="./css/style.css" />
  ```
- our first CSS rule. have them type it before explaining. **New Concept**: CSS rule structure (selector -> properties, braces, colons and semicolons).
  ```css
  body {
    font-family: 'Open Sans', sans-serif;
    font-weight: lighter;
    margin: 0;
  }
  ```
- reiterate about the tag selector. **New Concept**: Font & text properties (change the way text looks).
  ```css
  h2 {
    font-size: 35px;
    text-decoration: underline;
    text-underline-position: under;
  }

  h3 {
    font-size: 30px;
  }
  ```
- **New Concept**: Box model (every tag is a rectangle whose spacing can be changed). What happens if they increase the padding of `<ul>` or the margin of `<body>`?
  ```css
  ul {
    padding: 0;
    list-style: none;
  }
  ```

#### Header CSS ####
- now we turn our attention to the header. **New Concept**: percentage units
  ```css
  header {
    height: 100px;
    padding-left: 3%;
    padding-right: 3%;
    font-size: 25px;
  }
  ```
- how can we arrange the two elements of the header? **New Concept**: FLEXBOX (`justify-content` for horizontal arrangement & `align-items` for vertical arrangement). Show diagrams from CSS Tricks.
  ```css
  header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    /* ... */
  }
  ```
- details for the header. how can we select only the header's image? **New Concept**: descendant selector (allows for selecting more specifically).
  ```css
  header img {
    height: 75%;
  }
  ```
- more details for the header. **New Concept**: coloring text.
  ```css
  header a {
    margin-left: 25px;
    color: black;
    text-decoration: none;
  }
  ```
- final detail for the header. **New Concept**: hover selector.
  ```css
  header a:hover {
    text-decoration: underline;
  }
  ```

#### Big Section CSS ####
- how can we select only this `<section>` and not the others? **New Concept**: CLASS selectors (another way to select more specifically).
  ```css
  .big-section {
    display: flex;
    justify-content: center;
    align-items: center;
    text-align: center;
    height: 768px;
  }
  ```
- now for the background. download `background.jpg` into `images/`. **New Concept**: background image (size and position to adjust what we see).
  ```css
  .big-section {
    /* ... */
    background-image: url(../images/background.jpg);
    background-size: cover;
    background-position: bottom;
    color: white;
  }
  ```
- finishing up the details
  ```css
  .big-section h1 {
    font-size: 80px;
    margin-top: 0;
    margin-bottom: 40px;
  }

  .big-section p {
    font-size: 30px;
  }
  ```

#### Features CSS ####
- starting simple.
  ```css
  .features {
    text-align: center;
  }
  ```
- small but cool detail. **New Concept**: color hex codes (not every shade has a name so we need numbers).
  ```css
  .features h2 {
    text-decoration-color: #00c76f;
  }
  ```
- same color for the `<h3>` tags.
  ```css
  .features h3 {
    margin-top: 0;
    color: #00c76f;
  }
  ```
- flexbox helps again with the layout for the list.
  ```css
  .features ul {
    display: flex;
    justify-content: space-around;
    margin-top: 7%;
    margin-bottom: 7%;
  }

  .features li {
    width: 20%;
  }
  ```
- final adjustments
  ```css
  .features p {
    font-size: 25px;
  }

  .features img {
    width: 50%;
  }
  ```

#### Kanye CSS ####
- flexbox again for layout.
  ```css
  .kanye {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin: 3%;
    padding: 6%;
    background-color: #00c76f;
    color: white;
  }
  ```
- spacing adjustments.
  ```css
  .kanye h2 {
    margin-top: 0;
  }

  .kanye ul {
    width: 50%;
  }

  .kanye li {
    margin-bottom: 10%;
  }
  ```
- set the size of the small text.
  ```css
  .kanye p {
    font-size: 23px;
  }
  ```
- to the surprise of no one, kanye is out of control and needs to be kept in line.
  ```css
  .kanye img {
    width: 30%;
  }
  ```

**CSS done!**


### Part #4: Their Projects ###
- Direct them to the **attendee info page** again to find information about the two suggested landing page designs.
- Instruct them to **draw heavily from the Spotify example** and use **TAs as resources**.
- They have **two hours** to submit their design.
- Staff members will go around helping them submit (print to PDF and upload) or just check their designs.

**Good luck!**

CSS Selectors
CSS uses selectors to determine which elements the current set of styling should be applied to.

By Id
HTML
<body>
    <section id="intro">Welcome to my blog</section>
</body>
CSS
#intro {
    background-color: goldenrod;
    border: 1px solid black;
}
By Class
<body>
    <section class="title">Welcome to my blog</section>
</body>
CSS
.title {
    font-size: 1.85em;
    line-height: 1.2em;
}
Descendant Selector
HTML
<body>
  <article class="article">
    <section class="article__header">
      Welcome to my blog
    </section>
    <section class="article__content">
      Copper mug small batch meh plaid flexitarian. Before they
      sold out occupy chartreuse hot chicken, la croix
      fingerstache offal VHS air plant. Humblebrag blue bottle
      cred af jean shorts etsy copper mug chicharrones cronut
      art party scenester pabst chillwave. Distillery 8-bit
      pabst fashion axe, tousled cloud bread bushwick roof party
      franzen quinoa fixie.
    </section>
    <aside class="aside_box--dark dashed">
      <div class="article__header">
        Very important box header
      </div>
      Messenger bag sriracha tote bag intelligentsia air plant
      leggings.
    </aside>
    <section class="article__footer">
      Author: Steve Brownlee
    </section>
  </article>
</body>
CSS
/*
  This will select both of the article__header elements
*/
.article .article__header {
    font-size: 1.85em;
    line-height: 1.2em;
}

/*
  This will select only the section and ignore the div
*/
.article > .article__header {
    font-size: 1.85em;
    line-height: 1.2em;
}
Sibling Selector
/*
  This will select only a section that directly follows another section
*/
section + section {
  margin: 20px 0 10px 0;
}


/*
  This will select all sibling sections regardless if they are direct
*/
section ~ section {
  margin: 20px 0 10px 0;
}
Additional Reading
Child and Sibling Selectors
Videos to Watch
ID's vs Classes
W3Schools CSS Selectors Tutorial
CSS Basics — Advanced Selectors
CSS Combinator Selectors
CSS Tutorials #19 - Child Selectors
CSS POSITIONING (PART1)
Practice
These commands are a helpful quick start. You may choose to ignore them completely and create your own directory structure. If you choose to use this recommendation, just copy the commands below. It doesn't matter what directory you are currently in.

mkdir -p ~/workspace/css/exercises/css-selectors && cd $_
touch index.html
touch selectors.css
Paste the code below into your HTML document.

The header element should have a 1px, goldenrod border.
Convert the ul in the navigation element into a series of horizontal links with # as the href value, without bullets, and have some space between them horizontally.
Ensure that the navigation is semantically marked as such (i.e. wrap it in the correct HTML tag).
Any text in an element with class "disabled" should be colored grey, unless it is inside an anchor tag. If inside an anchor, it should be colored purple.
Any text inside an element with a class of "active" should be colored yellow.
Section elements should be contained within an article element.
There are two missing closing tags in this document. Make sure you add them back in.
Make the "I'm red" text colored red.
Make the "I'm blue" text colored blue.
The sibling h4 of the red element should have a background color of red.
The sibling h4 of the blue element should have background color of blue.
Any h4 that is a direct child of grandparent should have a 1px border with rounded corners.
Elements with a class of promo should have bold text that is also colored gold.
Without adding any other attributes to the input fields in the footer, write a CSS selector that makes any text input field have a height of 25px.
Note: You are not allowed to add id and class attributes to any component

<header>
  <ul>
    <li>Home</li>
    <li>Profile</li>
    <li>Blog</li>
  </ul>
</header>

<section>
  <div class="month-list">
    <ul>
      <li>
        <a href="#">January</a>
        <span class="disabled">My favorite month</span>
      </li>
      <li>
        <a href="#">
          <span class="active">February</span>
        </a>
      </li>
      <li>
        <a href="#">
          <span class="disabled">March</span>
        </a>
      </li>
      <li>
        <a href="#">April</a>
      </li>
      <li>
        <a href="#">
          <div class="promo">
            <span class="disabled">May</span>
          </div>
        </a>
      </li>
      <li>
        <a href="#">June</a>
      </li>
      <li>
        <a href="#">July</a>
      </li>
      <li>
        <a href="#">August</a>
        <span class="disabled">My least favorite month</span>
      </li>
      <li>
        <a href="#" class="disabled">September</a>
      </li>
    </ul>
  </div>
</section>

<section>
  <div class="grandparent">
    <div class="parent">
      <h4>Child of parent</h4>
      <div>
        <div>I'm red!</div>
        <h4>I'm red's sister
        <div>I'm blue!</div>
        <h4>I'm blue's brother</h4>
      </div>
    </div>
    <h4>Child of grandparent</h4>
  </div>
</section>

<footer class="padded">

  <div class="disclaimer">
    Only one purchase per household.
    <a href="#">
      <span class="footer-link">
        <span class="disabled">
          Privacy Policy
        </span>
      </span>
  </div>

  <div class="promo">
    Purchase a book today and receive the eBook for free!
  </div>

  <span>
      <input type="text" name="email" placeholder="Enter your email address">
      <input type="text" name="name" placeholder="Enter your name">
      <input type="tel" name="telephone" placeholder="Enter your telephone number">
  </span>

</footer> css-selecotrs

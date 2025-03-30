# HTML & CSS Course Assignment

## Project overview

Rainy Days webshop is made with HTML and CSS.

Link to Website: https://helenesyre.github.io/html-css-helene-syre/index.html

Link to Sketches: https://www.figma.com/proto/ahZPUy8EZcq06IduwEbLSk/(FM1AIDE10)-DES---Design?page-id=2%3A4&node-id=112-640&p=f&viewport=497%2C227%2C0.05&t=O7iVSwbjNlun6r3F-1&scaling=min-zoom&content-scaling=fixed&starting-point-node-id=112%3A640&show-proto-sidebar=1

> If you have trouble opening the Figma Prototype, try opening it in a different browser.

## Briefs

### Design 1

Rainy Days is an ecommerce website specializing in men's and women's rain jackets designed for various outdoor activities that enrich people's lives. With the slogan Pushing the Comfort Zone, the brand targets men and women aged 30 to 50 who enjoy outdoor adventures such as hiking, exploring, skiing, camping, and canoeing.

### HTML and CSS

For this assignment, I needed to create a fully functional and responsive website based on my Design 1 brief. It should include all the pages listed in the site architecture, and any functionality that would normally require JavaScript can be mimicked, like linking a login button to another page or have a generic “Coming Soon” page. The HTML should be clean and semantic, and the CSS should follow the DRY principle to keep it organized and readable. The site must be fully responsive, looking good on all screen sizes without horizontal scrolling, using Flexbox and CSS Grid. Accessibility is important, so the site should be WCAG compliant. Each page also needs a unique meta description, title, and H1. All code has to be written by me, but I can reference external sources for guidance as long as I document them in my report.

## Process

In the design course, I set out to make the website nice and structured. I had a hunch that we would have to code the website as the next project, but chose to take on the challenge rather than create a page I wasn't happy with just to make coding easier. The biggest challenges were how many elements I found out needed JS during the project. So I had to redo parts of the design during the project. This resulted in a lot more work than I had anticipated.

I quickly discovered how complicated the site was to set up without any previous experience. This made me very stressed. I therefore took the time I needed and feel I have learned an extremely large amount.

## WAVE Web Accessibility Tools & Markup Validation Service

### WAVE test

In some places during this test, I received alerts that I chose to ignore as these do not affect accessibility. Some examples:

- `Alerts - Redundant link` on all subpages, but not the front page. This is still clickable for everyone.
- `Alerts - Skipped heading level` on "Coming soon" pages as there is no other content on the pages than the nav, h1, p and footer.
- `Alerts - Possible heading` on the prices of the products as these are the same size as the product titles.
- `Alerts - Suspicious link text` here WAVE took the links as its starting point and not the elements around them, which made it seem like the links were read out of context.
- `Alerts - Underlined text` there will be separate subpages here at some point, but these have not been created. Thus, WAVE says that they should be removed unless there is a distinct need for it. I chose to keep them as I will create the subpages later.

### Color contrast problems

I started the project in design by having all text links in the yellow color I chose for the palette. I found out during testing with WAVE that this didn't work. So I used https://webaim.org/resources/contrastchecker/ to test the colors again, and ended up changing them to the "teal" color in the palette. The Contrast Ratio went from `2.02:1` to `5.67:1`.

### Validation test

During the validation process using the W3C Markup Validator, I received warnings related to HTML5 void elements. The issue was that I had used self-closing syntax (/>) for elements like <img /> and <meta />, which is common in XHTML but unnecessary in HTML5. While most browsers ignore the extra slash, it is considered unnecessary and triggered warnings in validation tools when i checked. To resolve this, I adjusted my code by removing the closing slash from affected elements.

### Accessibility problems

I quickly noticed that various elements on the page were not as easy to achieve as if we had used JS. The size selection on the jacket would not be selected with "tab" when the style was added. It works fine on mobile, iPad and PC when you click on it directly.

## Elements not made from the sketches

After testing and adjustments, I chose to disregard some elements from the sketches I made from the previous project. I chose to remove the animation on the cart buttons, as I wanted to focus on the coding this time and not the animation. Another thing I chose to remove here was the overlay to the map that shows an overview of the products that have been added to the checkout. I chose to remove this because we were not going to use javascript, which makes it more difficult to add the products you want to buy. This was also the reason why the animation on the buttons was not included. I removed the gradients in the background, even though I like them aesthetically, as I was unsure how to add them. On the front page and product page, I also removed the buttons on the image carousel, as I needed js for this.

Since we weren't going to use JavaScript, I came across several things that made it difficult to create fully functional elements. These were, for example: navigation, stepper in cart, products added to the checkout, removing or adding more products to the checkout, sorting filters (these have been added, but could have been added better with js), radio buttons on the image to change the information on the front page, selection of sizes and color of the jackets.

## Problem with Github pages

The Github Jekyll processing blocked the loading of files containing underscores such as `_variables.css`. To stop this from happening i added a `.nojekyll` file to the root of the project to disable the processing. Once the processing was disabled the site loaded correctly and the css files loaded with no issues.

> https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/about-github-pages-and-jekyll

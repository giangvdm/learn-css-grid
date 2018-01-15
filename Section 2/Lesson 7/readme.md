Lesson 7: Awesome Image Grid

// We start with the index.html file
// by adding a bunch of images inside the div.container
// Notice: all img(s) must be nested inside a div, for styling and positioning purposes
// So, by finishing, we should have our main content looking like this
<div class="container">
    <div><img></div>
    <div><img></div>
</div>

// Next up, we will work with the basic styling, that means anything rather than CSS Grid
// 1. Set the display of every div that contains the img to "flex"
// and make the content (img) inside it "center"
.container > div {
    display: flex;
    justify-content: center;
    align-items: center;
}
// 2. Make the img cover the whole div that nests it, and responsive
.container > div > img {
    width: 100%;
    height: 100%;
    object-fit: cover;
}

// Now to the CSS Grid part
// Start with very basic layout
.container {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(100px, 1fr));
    grid-gap: 5px;
}
// then we add in grid-auto-row to make sure every row of images is of the same size
.container {
    grid-auto-row: 100px;
}
// This part is important, and it's the new thing until now
.container {
    grid-auto-flow: dense;
}
// The grid-auto-flow attribute decides how all rows and columns will be positioned
// Currently it takes up the value "dense",
// that means all rows and columns will make sure to automatically fit themselves in every space that is possible
// grid-auto-flow default value is "row"

// We're basically done
// Let's move on to deal with the sizes of different images
// Some images are vertical, horizontal, some are big and deserve more attention
// so we add in classes, and make them stretch vertically, horizontally or to both sides
.vertical {
    grid-row: span 2;
}

.horizontal {
    grid-column: span 2;
}

.big {
    grid-column: span 2;
    grid-row: span 2;
}
// And then don't forget to add those classes to the divs that nest our images
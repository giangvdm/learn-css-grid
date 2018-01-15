Lesson 3: Positioning items

.container {
    grid-template-columns: repeat(2, 1fr); // our layout has 2 columns
}

selector {
    grid-column-start: 1;
    grid-column-end: 3; // it ends at 3
                        // since we have 2 columns, that means we have 3 column lines
                        // so if we want a row to take up the whole width of the page
                        // we set grid-column-end to (number-of-columns + 1) = (number-of-column-lines)
}

selector {
    grid-column: 1 / 3; // short-hand
    // or
    grid-column: 1 / span 2; // this makes more sense to stoopid human
}

selector {
    grid-column: 1 / -1; // but this is the best practice
                        // set end point to -1 rather than hard-code it to any other number
                        // because in the future, we might not know (or remember) how many columns we have in the layout
                        // the number -1 automatically make the row span through the whole width of the page
}

.container {
    // for flexibility, we make the layout to have 12 columns, 1fr each
    grid-template-columns: repeat(12, 1fr);
}

// then we select the specific element, and give it the custom width
// without hard-coding it with grid-template-columns: (for example) 1fr 3fr;
selector {
    grid-columns: 1 / 4;
}
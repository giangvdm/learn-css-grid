Lesson 4: Template Areas - great way to create prototypes of layout, to change and experiment layouts quickly

.container {
    // declare rows and columns as usual
    grid-template-rows: 1fr auto 1fr;
    grid-template-columns: repeat(12, 1fr);
    // new syntax
    grid-template-areas: 
        "h h h h h h h h h h h h"
        "m c c c c c c c c c c c"
        "f f f f f f f f f f f f";
        // this new syntax consists of bunch of strings
        // which "visualize" how the layout should look like // therefore this is a very great way create prototypes
        // we still need to declare rows and columns
        // and what the strings do, is name the area with specific "letters" as we do here
}

// next

selector {
    grid-area: h; // h stands for "header", so hereby we should select "#header"
}

// same thing goes on with other areas

// done and done
// your layout should look the same as we write code in the old way, which is
selector {
    grid-column: 1 / -1;
}

// you can add dots "." in those "prototype" strings to make the certain areas blank
        ". h h h h h h h h h h ."
        "m c c c c c c c c c c c"
        "f f f f f f f f f f f f";
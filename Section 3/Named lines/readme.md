Named lines

// When declaring templates for rows and columns
// we give those lines (between rows or between columns) names
// The syntax goes like this:
.container {
    grid-template-columns: [line-start-1] 1fr [line-start-2] 5fr [line-end-1 line-end-2];
}
// A line can have more than one name
// Different names are separated with a single space

// Then when we position areas like header, menu, content,...
// We "instruct" them where to start or end with named lines
#content {
    grid-column: cont-start / cont-end;
}

// We really should give lines names written in snake-case (hyphens separate words)
// because it's MAGIC!
// instead of grid-column: cont-start / cont-end; , which we have to set both the start and the end points
// we can write like this:
#content {
    grid-column: cont;
}
// it works the same way.

// We can also "wrap" the area by naming row lines
.container {
    grid-template-rows: [main-start] 1fr [cont-start] 4fr [cont-end] 1fr [main-end];
}
// and then, we use grid-area instead of just grid-column
#content {
    grid-area: cont;
}

// Notice that grid-area can only be used for area that is "wrapped" with row and column lines
// writing this
#footer {
    grid-area: main;
}
// for "unwrapped" area, will break the layout
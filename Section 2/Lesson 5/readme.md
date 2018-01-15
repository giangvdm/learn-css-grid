Lesson 5: Auto-fit and minmax

// Instead of hard-coding the number of rows or columns like this
.container {
    grid-template-columns: repeat(6, 1fr);
}
// we use auto-fit
.container {
    grid-template-columns: repeat(auto-fit, 1fr);
}
// auto-fit fills the screen with as many columns (or rows) as possible

// And
// if we hard-code the size of each row (or column), it might not be responsive
// there's something we can do with it, it's "minmax()"
.container {
    grid-template-columns: repeat(auto-fit, minmax(100px, 1fr));
}
// inside the minmax() method, we pass in 1 minimum and 1 maximum value of the size of each row (or column) we desire
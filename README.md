# h02-professional-portfolio
# CSS Grid Layout Module

CSS grid layout offers a module based layout system using rows and columns, which means no flexbox is needed!

## Wrapper

You must have a parent grid element to have rows and columns within that you can reference for layout. Here is an example of what you would write within the parent or "wrapper" element.

```bash
    display:grid;
    grid-template-columns:1fr 1fr;
    grid-auto-rows: minmax(100px, auto);
    grid-template: 
    'project1 project1'
    'project1 project1'
    'project2 project3'
    'project4 project5';
```

## When needed to place something within the grid using the method above you reference the class or id within css and name the area.

```bash
.class {
    grid-area: project1;
}
```
This sets that class to the space of project1 within the grid. It wont repeat within every space it is referenced within the template, rather it expands and will take up 4x as much space as the other projects. 

## Another method for making a grid

```bash
.wrapper{
    display: grid;
    grid-template-columns:1fr 2fr 2fr;
    grid-auto-rows: minmax(100px, auto);

}
```
This creates the grid with three columns one taking up 1/5 of the space and the other two taking up 2/5 of the space each. It also creates unlimited rows with 100px being the minimum height and auto being the max allowing them to expand to take up space.

The class reference or whatever you want to place within the grid would look like this

```bash
.box2{
    grid-column-start:1;
    grid-column-end:5;
    grid-row-start:2;
    grid-row-end:4;
}
```

The numbers refer to the lines within the "grid" the lines start as 1 at the left edge or top edge of the page and end at the right edge or bottom of the page. 

I chose to use grid because it was easier to understand than flexbox when needing to organize a layout of the page with. 

## Background Images for Projects
I set my background images within css because this allowed them to fully fill their grid space using 'cover' rather than messing up the layout

```bash
.p1 {
    grid-area: project1;
    border: 5px solid var(--blue);
    background: url(https://www.denverpost.com/wp-content/uploads/2019/06/TDP-L-SAND-DUNES-_HHR1128.JPG.jpg);
    background-size: cover;
}
```
This is how I set the background for the first project listed and did the same for subsequent projects

## Variables
I set variables within my CSS for repeating colors to allow for easy changes
```bash
:root {
    --blue: rgb(107, 187, 214);
    --grey:  rgb(67, 71, 75);
    --darkb: rgb(31, 31, 71);
}
```

## Links
I linked the navbar to push you to the correct section of the page using ids in html and I set the links in the footer to send you to perspective pages. I did not have the projects listed so I did not link anything from them. 
## Contributing
Image credits: 

https://www.denverpost.com/wp-content/uploads/2019/06/TDP-L-SAND-DUNES-_HHR1128.JPG.jpg

https://pblog.thrifty.com/wp-content/uploads/2018/01/img-hero-OLYMPICNP.jpg

https://national-park.com/wp-content/uploads/2016/04/Welcome-to-Grand-Canyon-National-Park.jpg

https://cdn.getyourguide.com/img/location/5c88db055a755.jpeg/88.jpg

https://upload.wikimedia.org/wikipedia/commons/thumb/0/0b/Black_Canyon_and_Gunnison_River_2008.jpg/1200px-Black_Canyon_and_Gunnison_River_2008.jpg


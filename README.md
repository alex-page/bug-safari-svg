# SVG feColorMatrix doesn't work in Safari when pulled in with a file

When using a file ( `filters.svg` ) file with the ID's of the filters you cannot do this in safari:
```
.filter{
  filter: url( "filters.svg#deuteranopia" );
}
```

You have to embed the svg into the HTML and use:
```
.filter{
  filter: url( "#deuteranopia" );
}
```
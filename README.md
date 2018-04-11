# 🐛  SVG feColorMatrix

> Safari feColorMatrix doesn't work in Safari with external a files


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
# 🐛  SVG feColorMatrix


> Safari feColorMatrix doesn't work with external a files


The example shows a red box three times:
- Box one is using an embedded svg
- Box two is using an svg file pointing to the ID
- Box three is the default state


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
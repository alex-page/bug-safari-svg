# 🐛  SVG feColorMatrix


> Safari feColorMatrix doesn't work with external a files


This issue was found in **Safari 11.1** and **Mac OS High Sierra 10.13.4**


This [example](https://alex-page.github.io/bug-safari-svg/) shows a red box three times:
- Box one adds a SVG filter using css to embedd a svg
- Box two adds a SVG filter using an external svg file with css pointing to file and ID
- Box three is the default state


When using a file ( `filters.svg` ) with the ID's of the filters you can not do this CSS in safari:
```css
.filter {
  filter: url( "filters.svg#deuteranopia" );
}
```

You have to embed the svg into the HTML and use this in CSS:
```css
.filter {
  filter: url( "#deuteranopia" );
}
```

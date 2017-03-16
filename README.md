# SVG (Scalable Vector Graphics)

### SVG Background:
* Developed in 1999  
* XML Vector Graphics Format  
* SVGs are scalable and customizable  
* Can create and edit with any text editor  
* Can be used with animation  
* High quality resolution no matter what size

### How to create your own SVGs

Start with the `<svg>` element tags  

The `<svg>` element can be embedded right into the HTML

```
<body>
  <svg width=" " height=" ">
    // element
  </svg>
</body>
```

Here is a list of elements that can be drawn inside the `<svg>` element:  
* Circle  
* Ellipse
* Rectangle  
* Line  
* Polyline  
* Polygon  
* Path  
* Text  

When styling these elements you will use different properties than your typical CSS properties that you're used to  

To specify a background color you will use the property `fill`  

To specify a border color you will use the property `stroke`  

To specify the border width you will use the property `stroke-width`  

```
fill="#2882f9" stroke="#000" stroke-width="3"
```

Shorthand styling:
```
style="fill:#2882f9;stroke:#000;stroke-width:3"
```

### Create a Circle

```
<svg width="110" height="100">
  <circle cx="50" cy="50" r="40" fill="#2882f9" stroke="#000" stroke-width="3" />
</svg>
```  

`cx` property defines the x-coordinate from the center of the circle  

`cy` property defines the y-coordinate from the center of the circle

`r` property defines the radius, which is the length of a line segment from the center to the perimeter  

### Create an Ellipse

```
<svg width="160" height="120">
  <ellipse cx="70" cy="60" rx="65" ry="50" fill="#ff5e5e" stroke="#000" stroke-width="3" />
</svg>
```  

`cx` and `cy` properties define the center of the ellipse  

`rx` property defines the wideness of the ellipse  

`ry` property defines the height of the ellipse

### Create a Rectangle

```
<svg width="140" height="100">
  <rect x="5" y="5" width="110" height="90" fill="#36e1ff" stroke="#000" stroke-width="3" />
</svg>
```  

If you want to create rounded corners you will need to add `rx` and `ry` properties  

### Create a Line

```
<svg height="100" width="100" viewBox="0 0 100 100">
  <line x1="5" y1="5" x2="50" y2="90" stroke="#000" stroke-width="5" />
</svg>
```  

`x1` (x-axis) and `y1` (y-axis) define the starting point of the line  

`x2` (x-axis) and `y2` (y-axis) define the ending point of the line  

### Create a Polyline

```
<svg height="100" width="100" viewBox="0 0 100 100">
  <line x1="5" y1="5" x2="50" y2="90" stroke="#000" stroke-width="3" />
</svg>
```  

Using the x-axis and y-axis you can set coordinates to create shapes with lines

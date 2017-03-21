# SVG (Scalable Vector Graphics)

[SVG Playground of Shapes](http://kirstenswanson.io/svg-shapes/)

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
    // element shape
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

An important concept to understand with SVGs is the `viewport` and `viewBox`.  

The `viewport` is the rectangular region of the SVG canvas, which is the viewing area the user will see. It is set by specifying the `width` and `height` properties of the SVG, which in turn determines the area of the coordinate system. By default the unit length is in pixels, but you can also use: `em`, `mm`, `pc`, `in` and `%`. The coordinate system starts in the top-left corner (0,0). If you increase the x-coordinate, the object will move towards the right. If you increase the y-coordinate, the object will move downwards.   

```
<svg width="100" height="100">  
  //element
</svg>
```  

The `viewBox` is initially placed on top of the `viewport`, but can be stretched or displaced to change the viewable region. The `viewBox` property takes four values: `min-x`, `min-y`, `width` and `height`.  

```
<svg width="100" height="100" viewBox="0 0 100 100">  
  //element
</svg>
```  

## Create a Circle

```
<svg width="110" height="100">
  <circle cx="50" cy="50" r="40" fill="#2882f9" stroke="#000" stroke-width="3" />
</svg>
```  

`cx` property defines the x-coordinate from the center of the circle  

`cy` property defines the y-coordinate from the center of the circle

`r` property defines the radius, which is the length of a line segment from the center to the perimeter  

## Create an Ellipse

```
<svg width="160" height="120">
  <ellipse cx="70" cy="60" rx="65" ry="50" fill="#ff5e5e" stroke="#000" stroke-width="3" />
</svg>
```  

`cx` and `cy` properties define the center of the ellipse  

`rx` property defines the wideness of the ellipse  

`ry` property defines the height of the ellipse

## Create a Rectangle

```
<svg width="140" height="100">
  <rect x="5" y="5" width="110" height="90" fill="#36e1ff" stroke="#000" stroke-width="3" />
</svg>
```  

If you want to create rounded corners you will need to add `rx` and `ry` properties  

## Create a Line

```
<svg height="100" width="100" viewBox="0 0 100 100">
  <line x1="5" y1="5" x2="50" y2="90" stroke="#000" stroke-width="5" />
</svg>
```  

`x1` (x-axis) and `y1` (y-axis) define the starting point of the line  

`x2` (x-axis) and `y2` (y-axis) define the ending point of the line  

## Create a Polyline

```
<svg height="100" width="100" viewBox="0 0 100 100">
  <line x1="5" y1="5" x2="50" y2="90" stroke="#000" stroke-width="3" />
</svg>
```  

Using the x-axis and y-axis you can set coordinates to create shapes with lines

## Create a Path

```
<svg height="100" width="100">
  <path d="M 10 40 C 90 -30 100 90 20 100 L 90 100 Z" fill="none" stroke="#000" stroke-width="3" />
</svg>
```

`<path>` element is a custom shape with curves, lines and arcs; imagine drawing a shape with a virtual pen going from point to point  

The `<path>` element can be grouped by wrapping the `<path>` elements in `<g>` tags

```
<svg height="100" width="100">
  <g>
    <path fill="none" stroke="#000" stroke-width="8" d="m 5,20 90,0" />
    <path fill="none" stroke="#000" stroke-width="8" d="m 5,45 90,0" />
    <path fill="none" stroke="#000" stroke-width="8" d="m 5,70 90,0" />
  </g>
</svg>
```

The `<path>` element takes specific commands with the `d` property, which you can think of the `d` representing the *path data*

* M = move to  
* L = line to
* V = vertical line   
* H = horizontal line
* C = curve to  
* S = smooth curve to  
* Q = quadratic Bézier curve  
* T = smooth quadratic Bézier curve
* A = elliptical arc  
* Z = close path  

*Uppercase letters represent `absolute` coordinate positioning and lowercase letters represent `relative` coordinate positioning based on the previous coordinate

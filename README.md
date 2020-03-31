# Sass Basics
## Sass Variables
Variables can be declared in Sass to store various types of data e.g. font sizes, colors, font types etc. See the example below for how variables are declared and assigned values.
```
$blue: #0000ff;
$red: #ff0000;
$green: #00ff00;
$big: 30px;
$regular: 20px;
$small: 10px;
$main-color:$blue
$main-size:$regular
```
Variables can be used to style elements, classes or ids. See example below:
```
h1{
  font-size: $big;
  color: $main
}
p{
  color: $green;
  font-size: $main-size;
}
```

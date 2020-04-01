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
$main-color: $blue;
$main-size: $regular;
```
Variables can be used to style elements, classes or ids. See example below:
```
h1{
  font-size: $big;
  color: $main;
}
p{
  color: $green;
  font-size: $main-size;
}

#container{
  color: $blue;
  font-size: $main-size;
}
```
## Mixins
Mixins are similar to javascript functions. They are reusable, and can take in parameters. Below is an example of a mixin and how it can be used:

```
@mixin formatText ($size, $color: $main){
  color: $color;
  font-size: $regular;
}

#testMixin{
  @include coloredHead(20px, $blue)
}
```
## Extending Styles
Predefined styles can be reused through extension when defining new styles. An example of how this can be done is shown below:
```
#extendedContainer{
  @extend #container;
  padding: 5px;
}
```
## Parent Selector
The ampersand symbol in Sass can be used when nesting to refer to the parent selector. An example of how it can be used is shown below:
```
#extendedContainer{
  @extend #container;
  padding: 5px;
  &:hover{
    background: $red;
  }
}
```
## Math Operations
Math operations such as addition, subtraction, multiplication and division can be performed using sass. Care should be taken not to mix units, or misuse subtraction as a hypen to form. Example of math operations in sass can be seen below:
```
$fontsize: 20px;

p{
  font-size: $fontsize;
}

h1{
  font-size: $fontsize * 2;
}

h2{
  font-size: $fontsize * 1.5;
}

li{
  font-size: $fontsize - 5;
}

.innercontainer{
  p{
    font-size: $fontsize/1.2;
    margin-top: (20px)/2;
  }
}
```
## Color Functions
Sass provides functions that can be used to get, set and manipulate colors. These functions are easy to use and can be very useful. A fulllist of these functions can be found [here](https://sass-lang.com/documentation/modules/color). And an example of their use is shown below:
```
$main: #1111AA;
$fontsize: 20px;

h1{
  background-color: $main;
  font-size: $fontsize * 2;
  &:hover{
    background-color:lighten($main, 50%);
  }
}
```


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

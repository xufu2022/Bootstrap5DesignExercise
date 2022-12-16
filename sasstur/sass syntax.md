# Variables

- Global Flag
  
```scss
// redefind global variables
// not for new vars
$p_color: red;
h1{
    $p_color: yellow !global;
    color:$p_color;
}
```

## Underscore vs hyphen

in varialbe names: _ equal -
```scss

$p_color: red;
$p-color: yellow;
h1{
    color:$p-color;
}
```

## Sass Nesting

```scss

.box{
    padding: 1em 2em;
    h1 {
        color: red;
    }
}
```

## Sass Partial

```scss

// _variable.scss
$bg: #000;
$primary: #373633;

//_bass.scss
@use "variable";
body{
    background: variables.$bg;
}

//style.scss
//start with an underscore _
//@use copies code
//namespaces and variable
//as shortcut
@use "variable" as var;
@use "base";
h1{
    color: var.$primary;
}
```

## Parent Selector

```scss

.box{
    padding: 1em 2em;
    h1 {
        color: red;
    } 
    // box-primary
     &-primary{
        background: #333;
     }
     // box inside container
     .container & {
        text-align: right;
     }
}
```
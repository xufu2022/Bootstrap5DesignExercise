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
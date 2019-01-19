# PostCSS Responsive Type

For implimenting responsive design using interpolation based off of responsive type by Sean King.  https://github.com/seaneking/postcss-responsive-type

I felt restricted and wished I could pass the property name as I had done using preprocessor mixins taken from http://madebymike.com.au/writing/precise-control-responsive-typography/


usage:
```
h3 {
  responsive: font-size inset 10;
  responsive: line-height outset 10;
}
  or

  responsive: font-size 1.3rem 1.55rem;

  or

  responsive: font-size 1.3rem 1.55rem 25rem 125rem;
```

where
  response: [property-name] [inset|outset] [10|20|30|40|50|60]

  or

  response: [property-name] [min-size] [max-size] [min-viewport-size] [max-viewport-size]


key'd sizes
```
  // min modular scale minor second
  // max >=40 modular scale minor second
  // max > 40 modular scale minor third
  outset: {
    10: {min: '3.38rem', max: '6rem'},
    20: {min: '2.66rem', max: '4.5rem'},
    30: {min: '2.25rem', max: '4rem'},
    40: {min: '1.7rem', max: '2rem'},
    50: {min: '1.5rem', max: '1.7rem'},
    60: {min: '1.3rem', max: '1.5rem'},
  },
  // min modular scale minor second
  // max >=40 modular scale minor second
  // max > 40 modular scale minor third
  inset: {
    10: {min: '1.618rem', max: '3.24rem'},
    20: {min: '1.46rem', max: '2.592rem'},
    30: {min: '1.32rem', max: '2.074rem'},
    40: {min: '1.138rem', max: '1.383rem'},
    50: {min: '1.067rem', max: '1.296rem'},
    60: {min: '1rem', max: '1.215rem'},
  },
  ```
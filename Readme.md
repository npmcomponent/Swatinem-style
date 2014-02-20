*This repository is a mirror of the [component](http://component.io) module [swatinem/style](http://github.com/swatinem/style). It has been modified to work with NPM+Browserify. You can install it using the command `npm install npmcomponent/swatinem-style`. Please do not open issues or send pull requests against this repo. If you have issues with this repo, report it to [npmcomponent](https://github.com/airportyh/npmcomponent).*

# Style

  Style Canvas renders using CSS.

## Installation

```
$ component install component/style
```

## Example

```css
body {
  font-size: 18px;
}
.progress {
  background: #fff;
}
.progress .percentage {
  color: #ddd;
}
```

```js
style('.progress', 'background-color');
// => 'rgb(255, 255, 255)'

style('.progress .percentage', 'color');
// => 'rgb(221, 221, 221)'

style('.progress .percent', 'font-size');
// => '18px'
```

## About

  This component exists so that you can influence aspects of your
  Canvas renders using CSS, where style decisions belong. For details
  view this [blog post](http://tjholowaychuk.com/post/6339741902/styling-canvas-drawings-with-css).

## Performance

  Generating and computing styles for ~2000 unique selectors in chrome
  takes ~300ms, so be careful if you plan on using this for many _unique_ selectors. Values
  are otherwise cached in an object and can easily operate above 300,000 ops/s.

## License

  MIT
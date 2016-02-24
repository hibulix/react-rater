# React-rater

Star rater

[Live demo](https://rawgit.com/ndyag/react-rater/master/example/index.html)

## install

Bower:

```sh
bower install react-rater
```

```html
<link rel="stylesheet" href="path/to/react-react.css">

<script src="path/to/react.js"></script>
<script src="path/to/react-dom.js"></script>
<script src="path/to/react-rater/dist/react-rater.js"></script>
<script>
  ReactDOM.render(
    React.createElement(ReactRater.default, {
      total: 5,
      rating: 2
    }), document.getElementById('app'))
</script>
```

NPM:

```
npm install react-rater
```

```js
import Rater from 'react-rater'

// ...
render() {
  return (<Rater total={5} rating={2} />)
}
```

## API

```html
<Rater total={} rating={} limit={} onRate={} />
```

All attributes are optional.

* `total`: default 5
* `rating`: default 0
* `limit`: default same as `total`. Sets the maximum rating value available.
* `onRate`: `function(rating, lastRating)`. Callback to retrieve rating value.

Notice: `onRate` is called on mousemove/click/mouseleave. Only for click `lastRating` has a value.

## Styling

### The CSS way

```scss
$react-rater-link: #ccc !default;   // color of star not rated
$react-rater-hover: #666 !default;  // color of star on hover
$react-rater-active: #000 !default; // color of star rated
```

### The JS way

`<Rater />` will repeat its children until counts reach `total`. https://github.com/NdYAG/react-rater/blob/master/src/index.js#L69

In this way you can define your own 'star' component (remember to check out [src/star.js](https://github.com/NdYAG/react-rater/blob/master/src%2Fstar.js)).

```
<Rater total={5}>
  <Heart />
</Rater>
```

## Real world example

Valentine's Day:

![Valentine](http://7d9o0k.com1.z0.glb.clouddn.com/valentine.png)

Abilu judge system for Douban Music:

![Abilu judge system for Douban Muisc](http://i.imgur.com/fbrX3mg.png)

## License

BSD.

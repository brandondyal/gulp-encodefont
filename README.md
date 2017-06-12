# gulp-injectfont [![Build Status](https://api.travis-ci.org/ddalcu/gulp-injectfont.svg?branch=master)](https://travis-ci.org/ddalcu/gulp-injectfont) [![NPM version](https://badge.fury.io/js/gulp-injectfont.png)](http://badge.fury.io/js/gulp-injectfont) [![GitHub version](https://badge.fury.io/gh/ddalcu%2Fgulp-injectfont.png)](http://badge.fury.io/gh/ddalcu%2Fgulp-injectfont)

Encode base64 data from font-files and store the result in a css file. Based on gulp-cssfont64

## Example


#### gulpfile.js

```js
var gulp = require('gulp');
var injectfont = require('gulp-injectfont');

gulp.task('default', function () {
	gulp.src('myfonts/*.ttf')
		.pipe(injectfont())
		.pipe(gulp.dest('path'));
});
```

#### content of "myfonts"-folder:

```html
	Roboto+Regular.ttf
```

#### output: path/Roboto+Regular.css

```html
	@font-face {font-family: Roboto Regular; src: url(data:application/x-font-ttf;base64,AABdboAvwAOAAFzugAvAA4AAXS6AJ8ADgABdLoAvwAOAAF0ugAPAA4AAXW6AC8ADgABdboALwAQAAFzugBfABAAAXO6AP8AEAABc7oAzwAQAAF0ugA/ABIAAXO6AA8AEgABc7oAsAASAAFzugB/ABIAAXO6AA8AEgABdLoAXwASAAF0ugB/ABIAAXW6AN8AEgABdLoAbwASAAF1ugAvABIAAXW6AD8AEgABdboA7wASAAF0ugCfABIAAXS6AB8AEgABdLoA7wASAAFzugAPABQAAXO6AB8AFAABc7oALwAUAAFzugA/ABQAAXO6AF8AFAABc7oAbwAUAAFzugB/ABQAAXO6AK8AFAABc7oAjwAUAAF0ugCvABQAAXS6AL8AFAABdLoAzwAUAAF0ugAvABQAAXW6AD8AFAABdQAA);}
```


### License

MIT

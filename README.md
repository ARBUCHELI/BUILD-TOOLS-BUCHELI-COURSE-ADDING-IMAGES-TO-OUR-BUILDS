# BUILD-TOOLS-BUCHELI-COURSE-ADDING-IMAGES-TO-OUR-BUILDS

Since Webpack 5, images and fonts no longer need a loader, and can use Webpack’s asset system. Their rules are similar to that of .txt files.

```
{
  test: /\.png$/i,
  type: 'asset/resource'
}
```

Notice we use type with asset/resource rather than asset/source. asset/resource creates a file in the build and imports it into the code as a URL. You may want to explore more 
about asset types.  The rule above would only match with *.png files, but we could have it handle many image types:

```
{
  test: /\.(png|svg|jpg|jpeg|gif)$/i,
  type: 'asset/resource'
}
```

When an image rule has been defined in webpack.config.js, we can import images into our JavaScript as if they were code:

```
import Square from '../square.png';
const img = 
document.createElement('img');
img.src = Square;
const body = 
document.querySelector('body');
body.appendChild(img);
```

```
npm install --save-dev style-loader css-loader
```

```
npm install --save-dev webpack-dev-server
```

```
npm run build
```

```
npm run start
```

# WebViewer

[PDFJS Express](https://pdfjs.express) is a powerful JavaScript-based PDF Library that wraps [PDF.js](https://mozilla.github.io/pdf.js/). It provides a slick out-of-the-box responsive UI that interacts with the core library to view, annotate and manipulate PDFs that can be embedded into any web project.

This version of the product is a PDF Viewer (no annotations) and is available to use for free. Get your free license on your [PDF.js Express Dashboard](https://pdfjs.express/profile).

![WebViewer UI](https://www.pdftron.com/downloads/pl/webviewer-ui.png)

## Usage

**1) Install PDFJS Express**
```
npm i @pdftron/pdfjs-express-viewer --save
```

This will also download all the assets that need to be included for PDFJS Express to work.

**2) Copy assets and resources to your public/static folder**

These assets need to be served with your application. For example, if your project is built into a `dist` folder, you could copy these assets into `dist/public`.

The folder you need to copy is `node_modules/@pdftron/pdfjs-express-viewer/public`.
```
cp -R ./node_modules/@pdftron/pdfjs-express-viewer/public ./dist
```

We recommend using a module bundler like [Webpack](https://webpack.js.org/) to automatically do this for you. There is a nice plugin called [copy-webpack-plugin](https://github.com/webpack-contrib/copy-webpack-plugin) that does just this.

**3) Import and instantiate WebViewer**

```js
import WebViewer from '@pdftron/pdfjs-express-viewer'

const element = document.getElementById('viewer');

WebViewer({
  path: '/public', // point to where the files you copied are served from
  initialDoc: 'https://pdftron.s3.amazonaws.com/downloads/pl/PDFTRON_about.pdf' // path to your document
}, element).then((instance) => {
  // Call APIs here
})
```

## Documentation
Full documentation for PDFJS Express can be found [here](https://pdfjs.express/documentation).
# 1st build bundle size = 1.12MB

npm install -save-dev webpack-bundle-analyzer

To webpack.config.js:

const BundleAnalyzerPlugin = require('webpack-bundle-analyzer').BundleAnalyzerPlugin;
const withreport = process.env.npm_config_withreport;

plugins:[
    withreport ? new BundleAnalyzerPlugin() : '',
]


Lastly, add a new script inside package json

"report": "npm run build --withreport true"


"npm run report" 


## SCOPE HOISTING
Scope hoisting uses a smarter way to add the modules to the bundle.

What scope hoisting can do:

> Makes the JavaScript execute faster in the browser
> Can reduce the bundle size

I got an error with this method

 > ​webpack.optimize.ModuleConcatenationPlugin()

 ## USE WEBPACK 4 IN PRODUCTION

module.exports = {
  entry: './index.js',
  mode: 'production',}
 # 2nd build bundle size = 137KB
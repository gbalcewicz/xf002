# xf002

[SOLVED] Q1: When running webpack, bundle is compiling to the output directory nicely, but when remove it, and start webpack-dev-server it cannot find the bundle file. When I modify the src/app.js the browser is reloading, but I cannot see that my bundle is present. I've tried with `--hot` and `--inline` flags too - no bundle loaded.

```
grzes@ayanami:/var/www/workspaces/xf002$ webpack-dev-server
http://localhost:8080/webpack-dev-server/
webpack result is served from /
content is served from /var/www/workspaces/xf002
Hash: abb10fe9ec18e6e122d7
Version: webpack 1.13.1
Time: 67ms
 Asset     Size  Chunks             Chunk Names
app.js  1.41 kB       0  [emitted]  main
chunk    {0} app.js (main) 21 bytes [rendered]
    [0] ./src/app.js 21 bytes {0} [built]
webpack: bundle is now VALID.

```
A1: The webpack.config has too have publicPath specified to the output folder

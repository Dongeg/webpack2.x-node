1.全局安装webpack && webpack-dev-server  

```
cnpm install webpack -g                                    //全局安装webpack
cnpm install -g webpack-dev-server  
```
2.项目安装 webpack-dev-server  

```
cnpm install --save-dev webpack-dev-server 
```
3.一般启动方式
```
//可能有时候需要手打，要不会报错
$ webpack-dev-server --inline --hot --port 9090
```

4.选项和参数

```
Config options:
  --config  Path to the config file
                          [字符串] [默认值: webpack.config.js or webpackfile.js]
  --env     Environment passed to the config, when it is a function

Basic options:
  --context    The root directory for resolving entry point and stats
                                        [字符串] [默认值: The current directory]
  --entry      The entry point                                          [字符串]
  --watch, -w  Watch the filesystem for changes                           [布尔]
  --debug      Switch loaders to debug mode                               [布尔]
  --devtool    Enable devtool for better debugging experience (Example:
               --devtool eval-cheap-module-source-map)                  [字符串]
  -d           shortcut for --debug --devtool eval-cheap-module-source-map
               --output-pathinfo                                          [布尔]
  -p           shortcut for --optimize-minimize --define
               process.env.NODE_ENV="production"                          [布尔]
  --progress   Print compilation progress in percentage                   [布尔]

Module options:
  --module-bind       Bind an extension to a loader                     [字符串]
  --module-bind-post                                                    [字符串]
  --module-bind-pre                                                     [字符串]

Output options:
  --output-path                 The output path for compilation assets
                                        [字符串] [默认值: The current directory]
  --output-filename             The output filename of the bundle
                                                    [字符串] [默认值: [name].js]
  --output-chunk-filename       The output filename for additional chunks
        [字符串] [默认值: filename with [id] instead of [name] or [id] prefixed]
  --output-source-map-filename  The output filename for the SourceMap   [字符串]
  --output-public-path          The public path for the assets          [字符串]
  --output-jsonp-function       The name of the jsonp function used for chunk
                                loading                                 [字符串]
  --output-pathinfo             Include a comment with the request for every
                                dependency (require, import, etc.)        [布尔]
  --output-library              Expose the exports of the entry point as library
                                                                        [字符串]
  --output-library-target       The type for exposing the exports of the entry
                                point as library                        [字符串]

Advanced options:
  --records-input-path       Path to the records file (reading)         [字符串]
  --records-output-path      Path to the records file (writing)         [字符串]
  --records-path             Path to the records file                   [字符串]
  --define                   Define any free var in the bundle          [字符串]
  --target                   The targeted execution environment         [字符串]
  --cache                    Enable in memory caching
                          [布尔] [默认值: It's enabled by default when watching]
  --watch-stdin, --stdin     close when stdin ends                        [布尔]
  --watch-aggregate-timeout  Timeout for gathering changes while watching
  --watch-poll               The polling interval for watching (also enable
                             polling)                                     [布尔]
  --hot                      Enables Hot Module Replacement               [布尔]
  --prefetch                 Prefetch this request (Example: --prefetch
                             ./file.js)                                 [字符串]
  --provide                  Provide these modules as free vars in all modules
                             (Example: --provide jQuery=jquery)         [字符串]
  --labeled-modules          Enables labeled modules                      [布尔]
  --plugin                   Load this plugin                           [字符串]
  --bail                     Abort the compilation on first error         [布尔]
  --profile                  Profile the compilation and include information in
                             stats                                        [布尔]
  --hot-only                 Do not refresh page if HMR fails             [布尔]

Resolving options:
  --resolve-alias         Setup a module alias for resolving (Example:
                          jquery-plugin=jquery.plugin)                  [字符串]
  --resolve-extensions    Setup extensions that should be used to resolve
                          modules (Example: --resolve-extensions .es6 .js)[数组]
  --resolve-loader-alias  Setup a loader alias for resolving            [字符串]

Optimizing options:
  --optimize-max-chunks      Try to keep the chunk count below a limit
  --optimize-min-chunk-size  Try to keep the chunk size above a limit
  --optimize-minimize        Minimize javascript and switches loaders to
                             minimizing                                   [布尔]

Stats options:
  --color, --colors   Enables/Disables colors on the console
                                               [布尔] [默认值: (supports-color)]
  --info              Info                                 [布尔] [默认值: true]
  --quiet             Quiet                                               [布尔]
  --client-log-level  Log level in the browser (info, warning, error or none)
                                                       [字符串] [默认值: "info"]

SSL options:
  --https           HTTPS                                                 [布尔]
  --key             Path to a SSL key.                                  [字符串]
  --cert            Path to a SSL certificate.                          [字符串]
  --cacert          Path to a SSL CA certificate.                       [字符串]
  --pfx             Path to a SSL pfx file.                             [字符串]
  --pfx-passphrase  Passphrase for pfx file.                            [字符串]

Response options:
  --content-base          A directory or URL to serve HTML content from.[字符串]
  --watch-content-base    Enable live-reloading of the content-base.      [布尔]
  --history-api-fallback  Fallback to /index.html for Single Page Applications.
                                                                          [布尔]
  --compress              Enable gzip compression                         [布尔]

Connection options:
  --port    The port
  --socket  Socket to listen
  --public  The public hostname/ip address of the server                [字符串]
  --host    The hostname/ip address the server will bind to
                                                  [字符串] [默认值: "localhost"]

选项：
  --help, -h     显示帮助信息                                             [布尔]
  --version, -v  显示版本号                                               [布尔]
  --lazy         Lazy                                                     [布尔]
  --inline       Inline mode (set to false to disable including client scripts
                 like livereload)                          [布尔] [默认值: true]
  --open         Open default browser     
```

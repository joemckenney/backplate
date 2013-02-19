Backplate
===========

A boilerplate for managing the development source tree and production build of a RequireJS driven Backbone application.
RequireJS configuration is mostly shared between both development and production. 

For convenience Backplate ships with Backbone, underscore, jQuery, RequireJS, r.js (RequireJS optimizer), almond, text.js (RequireJS text plugin) 
and pre-configured RequireJS shims for non-AMD compliant packages.

Development:
```sh
[docyes@len backplate]$ firefox src/debug.html
```

Production:
```sh
[docyes@len backplate]$ ./build.sh 

Tracing dependencies for: main
Uglifying file: /home/docyes/code/backplate/build/js/require.config.js
Uglifying file: /home/docyes/code/backplate/build/js/contrib/require.js
Uglifying file: /home/docyes/code/backplate/build/js/contrib/text.js
Uglifying file: /home/docyes/code/backplate/build/js/main.js

js/main.js
----------------
js/contrib/almond.js
js/contrib/underscore.js
js/contrib/jquery.js
js/contrib/backbone.js
js/main.js

[docyes@len backplate]$ firefox build/index.html
```

File System Reference:
```sh
./lib: -> Shared libraries 
r.js -> RequireJS optimizer

./src: -> Project source tree
debug.html -> Development runtime (uses full feature RequireJS package)
index.html -> Production runtime (uses minimal almond package)

js -> JavaScript source tree
main.js -> Program main startup
require.config.js -> General shared RequireJS configuration
```




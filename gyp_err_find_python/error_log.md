```
 => [internal] load build definition from Dockerfile                                                                                                                                  0.0s
 => => transferring dockerfile: 218B                                                                                                                                                  0.0s
 => [internal] load .dockerignore                                                                                                                                                     0.0s
 => => transferring context: 145B                                                                                                                                                     0.0s
 => [internal] load metadata for docker.io/library/node:14-alpine                                                                                                                     1.0s
 => [1/8] FROM docker.io/library/node:14-alpine@sha256:2c6a909495ef3761328c10945cbe84c06d079f7ca49dc24271e73be8cab85ad7                                                               0.0s
 => [internal] load build context                                                                                                                                                     0.0s
 => => transferring context: 297.88kB                                                                                                                                                 0.0s
 => CACHED [2/8] WORKDIR /app                                                                                                                                                         0.0s
 => CACHED [3/8] RUN pwd                                                                                                                                                              0.0s
 => CACHED [4/8] ADD package*.json ./                                                                                                                                                 0.0s
 => CACHED [5/8] RUN ls                                                                                                                                                               0.0s
 => ERROR [6/8] RUN npm install                                                                                                                                                       4.5s
------                                                                                                                                                                                     
 > [6/8] RUN npm install:                                                                                                                                                                  
#10 0.395 npm WARN read-shrinkwrap This version of npm is compatible with lockfileVersion@1, but package-lock.json was generated for lockfileVersion@2. I'll try to do my best with it!    
#10 3.459                                                                                                                                                                                  
#10 3.459 > bcrypt@5.0.1 install /app/node_modules/bcrypt                                                                                                                                  
#10 3.459 > node-pre-gyp install --fallback-to-build                                                                                                                                       
#10 3.459 
#10 4.123 node-pre-gyp ERR! install response status 404 Not Found on https://github.com/kelektiv/node.bcrypt.js/releases/download/v5.0.1/bcrypt_lib-v5.0.1-napi-v3-linux-arm64-musl.tar.gz 
#10 4.124 node-pre-gyp WARN Pre-built binaries not installable for bcrypt@5.0.1 and node@14.21.2 (node-v83 ABI, musl) (falling back to source compile with node-gyp) 
#10 4.124 node-pre-gyp WARN Hit error response status 404 Not Found on https://github.com/kelektiv/node.bcrypt.js/releases/download/v5.0.1/bcrypt_lib-v5.0.1-napi-v3-linux-arm64-musl.tar.gz 
#10 4.295 gyp ERR! find Python 
#10 4.295 gyp ERR! find Python Python is not set from command line or npm configuration
#10 4.295 gyp ERR! find Python Python is not set from environment variable PYTHON
#10 4.295 gyp ERR! find Python checking if "python" can be used
#10 4.295 gyp ERR! find Python - "python" is not in PATH or produced an error
#10 4.295 gyp ERR! find Python checking if "python2" can be used
#10 4.295 gyp ERR! find Python - "python2" is not in PATH or produced an error
#10 4.295 gyp ERR! find Python checking if "python3" can be used
#10 4.295 gyp ERR! find Python - "python3" is not in PATH or produced an error
#10 4.295 gyp ERR! find Python 
#10 4.295 gyp ERR! find Python **********************************************************
#10 4.295 gyp ERR! find Python You need to install the latest version of Python.
#10 4.295 gyp ERR! find Python Node-gyp should be able to find and use Python. If not,
#10 4.295 gyp ERR! find Python you can try one of the following options:
#10 4.295 gyp ERR! find Python - Use the switch --python="/path/to/pythonexecutable"
#10 4.295 gyp ERR! find Python   (accepted by both node-gyp and npm)
#10 4.295 gyp ERR! find Python - Set the environment variable PYTHON
#10 4.295 gyp ERR! find Python - Set the npm configuration variable python:
#10 4.295 gyp ERR! find Python   npm config set python "/path/to/pythonexecutable"
#10 4.295 gyp ERR! find Python For more information consult the documentation at:
#10 4.295 gyp ERR! find Python https://github.com/nodejs/node-gyp#installation
#10 4.295 gyp ERR! find Python **********************************************************
#10 4.295 gyp ERR! find Python 
#10 4.295 gyp ERR! configure error 
#10 4.296 gyp ERR! stack Error: Could not find any Python installation to use
#10 4.296 gyp ERR! stack     at PythonFinder.fail (/usr/local/lib/node_modules/npm/node_modules/node-gyp/lib/find-python.js:307:47)
#10 4.296 gyp ERR! stack     at PythonFinder.runChecks (/usr/local/lib/node_modules/npm/node_modules/node-gyp/lib/find-python.js:136:21)
#10 4.296 gyp ERR! stack     at PythonFinder.<anonymous> (/usr/local/lib/node_modules/npm/node_modules/node-gyp/lib/find-python.js:179:16)
#10 4.296 gyp ERR! stack     at PythonFinder.execFileCallback (/usr/local/lib/node_modules/npm/node_modules/node-gyp/lib/find-python.js:271:16)
#10 4.296 gyp ERR! stack     at exithandler (child_process.js:390:5)
#10 4.296 gyp ERR! stack     at ChildProcess.errorhandler (child_process.js:402:5)
#10 4.296 gyp ERR! stack     at ChildProcess.emit (events.js:400:28)
#10 4.296 gyp ERR! stack     at Process.ChildProcess._handle.onexit (internal/child_process.js:283:12)
#10 4.296 gyp ERR! stack     at onErrorNT (internal/child_process.js:472:16)
#10 4.296 gyp ERR! stack     at processTicksAndRejections (internal/process/task_queues.js:82:21)
#10 4.296 gyp ERR! System Linux 5.15.49-linuxkit
#10 4.296 gyp ERR! command "/usr/local/bin/node" "/usr/local/lib/node_modules/npm/node_modules/node-gyp/bin/node-gyp.js" "configure" "--fallback-to-build" "--module=/app/node_modules/bcrypt/lib/binding/napi-v3/bcrypt_lib.node" "--module_name=bcrypt_lib" "--module_path=/app/node_modules/bcrypt/lib/binding/napi-v3" "--napi_version=8" "--node_abi_napi=napi" "--napi_build_version=3" "--node_napi_label=napi-v3"
#10 4.296 gyp ERR! cwd /app/node_modules/bcrypt
#10 4.296 gyp ERR! node -v v14.21.2
#10 4.296 gyp ERR! node-gyp -v v5.1.0
#10 4.296 gyp ERR! not ok 
#10 4.298 node-pre-gyp ERR! build error 
#10 4.299 node-pre-gyp ERR! stack Error: Failed to execute '/usr/local/bin/node /usr/local/lib/node_modules/npm/node_modules/node-gyp/bin/node-gyp.js configure --fallback-to-build --module=/app/node_modules/bcrypt/lib/binding/napi-v3/bcrypt_lib.node --module_name=bcrypt_lib --module_path=/app/node_modules/bcrypt/lib/binding/napi-v3 --napi_version=8 --node_abi_napi=napi --napi_build_version=3 --node_napi_label=napi-v3' (1)
#10 4.299 node-pre-gyp ERR! stack     at ChildProcess.<anonymous> (/app/node_modules/@mapbox/node-pre-gyp/lib/util/compile.js:89:23)
#10 4.299 node-pre-gyp ERR! stack     at ChildProcess.emit (events.js:400:28)
#10 4.299 node-pre-gyp ERR! stack     at maybeClose (internal/child_process.js:1088:16)
#10 4.299 node-pre-gyp ERR! stack     at Process.ChildProcess._handle.onexit (internal/child_process.js:296:5)
#10 4.299 node-pre-gyp ERR! System Linux 5.15.49-linuxkit
#10 4.299 node-pre-gyp ERR! command "/usr/local/bin/node" "/app/node_modules/.bin/node-pre-gyp" "install" "--fallback-to-build"
#10 4.299 node-pre-gyp ERR! cwd /app/node_modules/bcrypt
#10 4.299 node-pre-gyp ERR! node -v v14.21.2
#10 4.299 node-pre-gyp ERR! node-pre-gyp -v v1.0.9
#10 4.299 node-pre-gyp ERR! not ok 
#10 4.299 Failed to execute '/usr/local/bin/node /usr/local/lib/node_modules/npm/node_modules/node-gyp/bin/node-gyp.js configure --fallback-to-build --module=/app/node_modules/bcrypt/lib/binding/napi-v3/bcrypt_lib.node --module_name=bcrypt_lib --module_path=/app/node_modules/bcrypt/lib/binding/napi-v3 --napi_version=8 --node_abi_napi=napi --napi_build_version=3 --node_napi_label=napi-v3' (1)
#10 4.403 npm WARN optional SKIPPING OPTIONAL DEPENDENCY: fsevents@2.3.2 (node_modules/fsevents):
#10 4.403 npm WARN notsup SKIPPING OPTIONAL DEPENDENCY: Unsupported platform for fsevents@2.3.2: wanted {"os":"darwin","arch":"any"} (current: {"os":"linux","arch":"arm64"})
#10 4.403 
#10 4.418 npm ERR! code ELIFECYCLE
#10 4.418 npm ERR! errno 1
#10 4.421 npm ERR! bcrypt@5.0.1 install: `node-pre-gyp install --fallback-to-build`
#10 4.421 npm ERR! Exit status 1
#10 4.421 npm ERR! 
#10 4.421 npm ERR! Failed at the bcrypt@5.0.1 install script.
#10 4.421 npm ERR! This is probably not a problem with npm. There is likely additional logging output above.
#10 4.433 
#10 4.433 npm ERR! A complete log of this run can be found in:
#10 4.433 npm ERR!     /root/.npm/_logs/2023-01-19T18_41_01_543Z-debug.log
------
executor failed running [/bin/sh -c npm install]: exit code: 1
```
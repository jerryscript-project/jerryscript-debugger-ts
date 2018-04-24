# JerryScript Debugger & Chrome DevTools Proxy
[![License](https://img.shields.io/badge/licence-Apache%202.0-brightgreen.svg?style=flat)](LICENSE)
[![Build Status](https://travis-ci.org/jerryscript-project/jerryscript-debugger-ts.svg?branch=master)](https://travis-ci.org/jerryscript-project/jerryscript-debugger-ts)
[![IRC Channel](https://img.shields.io/badge/chat-on%20freenode-brightgreen.svg)](https://kiwiirc.com/client/irc.freenode.net/#jerryscript)

## Dependencies

- node.js
- `yarn` or `npm` (the steps below use `yarn`)

## Installing

```
$ cd jerryscript-debugger-ts
$ yarn install
```

## Building in watch mode

This will make the TypeScript compiler monitor the source files and re-build
files whenever there is a change.

```
$ cd jerryscript-debugger-ts
$ yarn build:watch
```

## Running tests

```
$ cd jerryscript-debugger-ts
$ yarn test
```

## Running tests in watch mode

This will make the test runner monitor the source files and re-run the tests
whenever there is a change.

```
$ cd jerryscript-debugger-ts
$ yarn test:watch
```

## Running the linter

```
$ cd jerryscript-debugger-ts
$ yarn lint
```

## Using

Build and run JerryScript with the debugger enabled. For example, with the
JerryScript Linux build:
```bash
$ cd jerryscript
$ python tools/build.py --jerry-debugger=on --jerry-libc=off
$ ./build/bin/jerry --start-debug-server --log-level 2 /path/to/source.js
```

Have Chrome running and visit the URL `chrome://inspect`, and click
"Open dedicated DevTools for Node."

Finally, run this project's proxy application:
```bash
$ cd jerryscript-debugger-ts
$ ./jerry-debugger.sh
```

This should connect to the debugger and give focus to the DevTools window to
start debugging.

## Contributing
The project can only accept contributions which are licensed under the [Apache License 2.0](LICENSE) and are signed according to the JerryScript [Developer's Certificate of Origin](DCO.md). For further information please see our [Contribution Guidelines](CONTRIBUTING.md).

## License
This library is open source software under the [Apache License 2.0](LICENSE). Complete license and copyright information can be found in the source code.

> Copyright JS Foundation and other contributors, http://js.foundation

> Licensed under the Apache License, Version 2.0 (the "License"); you may not use this file except in compliance with the License. You may obtain a copy of the License at http://www.apache.org/licenses/LICENSE-2.0 Unless required by applicable law or agreed to in writing, software distributed under the License is distributed on an "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied. See the License for the specific language governing permissions and limitations under the License.

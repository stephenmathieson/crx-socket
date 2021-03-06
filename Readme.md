
# crx-socket

  Messaging sockets for Chrome extensions with a usable API.

## Installation

  Install with [component(1)](http://component.io):

    $ component install stephenmathieson/crx-socket

## API

### createServer(name)

  Create a `Server` with `name`.

#### Server#broadcast(data)

  Send a message to all connected ports with `data`.

#### Server#on(name, fn)

  Respond to `name` messages with `fn`.

#### Server#once(name, fn)

  Respond to `name` messages with `fn`, but only once. 

#### Server#off(name, fn)

  Stop `fn` from responding to `name` messages.

### createClient(name)

  Create a `Client` with `name`.

#### Client#emit(name, [data], [fn])

  Emit a `name` message with the given `data`, optionally invoking `fn(response)`.

#### Client#on(name, fn)

  Listen for the given `name` message with `fn`.

#### Client#once(name, fn)

  Listen for the given `name` message, but only fire `fn` once.

#### Client#off(name, [fn])

  Remove the given `fn` listener for `name` messages, or all `name` listeners if `fn` is not provided.

## Example

  Run `make -C test`, then open `test/bundles` as an unpacked extension.

## License

  The MIT License (MIT)

  Copyright (c) 2014 Stephen Mathieson &lt;me@stephenmathieson.com&gt;

  Permission is hereby granted, free of charge, to any person obtaining a copy
  of this software and associated documentation files (the "Software"), to deal
  in the Software without restriction, including without limitation the rights
  to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
  copies of the Software, and to permit persons to whom the Software is
  furnished to do so, subject to the following conditions:

  The above copyright notice and this permission notice shall be included in
  all copies or substantial portions of the Software.

  THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
  IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
  FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
  AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
  LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
  OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
  THE SOFTWARE.
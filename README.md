# bloodhound-utils

Two wrapper scripts around getting a [BloodHound](https://github.com/BloodHoundAD/BloodHound) database and client up and running


## Usage

### Server

```bash
$ bloodhound-server foo.graphdb
```

* If `foo.graphdb` does not exist a new database will be created.
* The [neo4j](https://hub.docker.com/_/neo4j/) Docker image will be launched (interactively; use CTRL-C to exit)

### Client

```bash
$ bloodhound-client
```

* If there isn't a BloodHound release in `.`, `/opt` or `/usr/local` then it will be downloaded
* The BloodHound client will be launched


## Installation

Currently Linux and OSX are supported:

```bash
git clone https://github.com/0x6c7862/bloodhound-utils
cd bloodhound-utils
for f in bloodhound-{client,server}; do sudo cp "${f}" /usr/local/bin; done
```

`bloodhound-server` depends on [`docker`](https://www.docker.com/). See website for details on installation.


## Contributing

### Bug Reports & Feature Requests

Please use the [issue tracker](https://github.com/0x6c7862/bloodhound-utils/issues) to report any bugs or file feature requests.

### Developing

Pull requests are welcome!

### License

This is free and unencumbered software released into the public domain.

Anyone is free to copy, modify, publish, use, compile, sell, or
distribute this software, either in source code form or as a compiled
binary, for any purpose, commercial or non-commercial, and by any
means.

In jurisdictions that recognize copyright laws, the author or authors
of this software dedicate any and all copyright interest in the
software to the public domain. We make this dedication for the benefit
of the public at large and to the detriment of our heirs and
successors. We intend this dedication to be an overt act of
relinquishment in perpetuity of all present and future rights to this
software under copyright law.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF
MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT.
IN NO EVENT SHALL THE AUTHORS BE LIABLE FOR ANY CLAIM, DAMAGES OR
OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE,
ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR
OTHER DEALINGS IN THE SOFTWARE.

For more information, please refer to <http://unlicense.org/>

### BloodHound License

BloodHound uses graph theory to reveal hidden relationships and attack paths in
an Active Directory environment. Copyright (C) 2016 Andrew Robbins, Rohan
Vazarkar, Will Schroeder

This program is free software: you can redistribute it and/or modify it under
the terms of the GNU General Public License as published by the Free Software
Foundation, either version 3 of the License, or (at your option) any later
version.

This program is distributed in the hope that it will be useful, but WITHOUT ANY
WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A
PARTICULAR PURPOSE. See the GNU General Public License for more details.

You should have received a copy of the GNU General Public License along with
this program. If not, see http://www.gnu.org/licenses/.

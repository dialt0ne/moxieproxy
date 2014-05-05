moxieproxy Cookbook
====================

This cookbook installs and configures moxi-server

![Make Mine Moxie](https://upload.wikimedia.org/wikipedia/en/3/3a/Moxie_logo.jpg)

Requirements
------------

#### packages
- `moxi-server` - moxieproxy needs to install the moxi-server package

Attributes
----------

#### moxieproxy::default
<table>
  <tr>
    <th>Key</th>
    <th>Type</th>
    <th>Description</th>
    <th>Default</th>
  </tr>
  <tr>
    <td><tt>['moxieproxy']['bindport']</tt></td>
    <td>Int</td>
    <td>Port that moxi-server listens on</td>
    <td><tt>11211</tt></td>
  </tr>
  <tr>
    <td><tt>['moxieproxy']['servers']</tt></td>
    <td>Array</td>
    <td>List of servers that moxi-server will connect to</td>
    <td><tt>nil</tt></td>
  </tr>
</table>

Usage
-----
#### moxieproxy::default

Just include `moxieproxy` in your node's `run_list` and set attributes:

```json
{
  "name":"my_node",
  "run_list": [
    "recipe[moxieproxy]"
  ],
  "moxieproxy": {
    "bindport": "11211",
    "servers": [
      "cache-a.example.com:11211",
      "cache-b.example.com:11211",
      "cache-c.example.com:11211"
    ]
  },
}
```

Contributing
------------

1. Fork the repository on Github
2. Create a named feature branch (like `add_component_x`)
3. Write your change
4. Write tests for your change (if applicable)
5. Run the tests, ensuring they all pass
6. Submit a Pull Request using Github

License and Authors
-------------------
Authors: Anthony Tonns <atonns@corsis.com>

   Copyright 2014 Corsis
   http://www.corsis.com/

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       http://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.


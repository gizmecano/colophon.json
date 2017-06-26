# colophon.json

## overview

When working on a web project, it can be needed or simply useful to maintain some basic informations: **colophon.json** is a tiny schema which aims to simply store these main static data using a [JSON](http://www.json.org/) formatted file.

## implementation

Implementing this file is easy: for example, using PHP, after having defined the root path of the project, use `json_decode` to take the JSON encoded string and convert it into a variable.

Example:

```php
<?php
  $colophon = json_decode(file_get_contents(ROOT_PATH.'/colophon.json'),true);
```

Then, using any of the data which are stored in the file can be done really easily when needed.

Example:

```xml
  <ul>
    <li>Version <?php echo $colophon['release']['version']; ?></li>
  </ul>
```

## license

colophon.json: a tiny schema for storing main static data of a web project

--------------------------------------------------------------------------------

Copyright © 2017 P. Mergey

This program is free software: you can redistribute it and/or modify it under the terms of the [GNU General Public License](LICENSE) as published by the Free Software Foundation, either version 3 of the License, or (at your option) any later version.

This program is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the [GNU General Public License](LICENSE) for more details.

You should have received a copy of the [GNU General Public License](LICENSE) along with this program. If not, see [this page](http://www.gnu.org/licenses/gpl-3.0.txt).

# 1\. `matter`

- _Type_: `object`
- _Scope_: main data which permit to exactly identify the project

## 1.1 `name`

- _Type_: `string`
- _Scope_: simplified naming of the project, containing the main words and the major version number, only separated by dashes and/or dots

## 1.2 `title`

- _Type_: `string`
- _Scope_: exact wording of the project, with admissible required spaces and/or punctuations

## 1.3 `link`

- _Type_: `string`
- _Scope_: official homepage of the project

--------------------------------------------------------------------------------

Example:

```json
{
  "matter": {
    "name": "portfolio-3",
    "title": "Porfolio of Aulus Agerius",
    "link": "http://www.aulo-agerio.net/"
  }
}
```

# 2\. `people`

- _Type_: `object` or `array`
- _Scope_: data relating to the persons who have contributed to or were concerned by the project

## 2.1 `name`

- _Type_: `string`
- _Scope_: unique name for identifying the concerned person

## 2.2 `role`

- _Type_: `string`
- _Scope_: specific role in the project or during the building process, such as `"owner"`, `"author"`, `"developer"`, `"translator"`, etc.

## 2.3 `link`

- _Type_: `string` or `NULL`
- _Scope_: link to the homepage of the concerned person

--------------------------------------------------------------------------------

Example (with `array`):

```json
{
  "people": [
    {
      "name": "Aulus Agerius",
      "role": "owner",
      "link": "http://www.aulo-agerio.net/"
    },
    {
      "name": "Numerius Negidius",
      "role": "author",
      "link": "http://www.numerium-negidium.net/"
    }
  ]
}
```

# 3\. `release`

- _Type_: `object`
- _Scope_: specific data regarding the latest iteration of the project

## 3.1 `version`

- _Type_: `string`
- _Scope_: version number of the release, using incremental [semantic versioning](http://semver.org/) format (_i.e._ `Major.Minor.Patch`)

## 3.2 `pubdate`

- _Type_: `string`
- _Scope_: release date of the release, using parsable [ISO 8601](http://www.iso.org/iso/home/standards/iso8601.htm) format (_i.e._ `YYYY-MM-DD`)

--------------------------------------------------------------------------------

Example:

```json
{
  "release": {
      "version": "3.2.1",
      "pubdate": "2017-06-22"
    }
}
```

# 4\. `license`

- _Type_: `string`
- _Scope_: license of the project, using [SPDX short identifiers](https://spdx.org/licenses/) for open source and `"proprietary"` for closed source

--------------------------------------------------------------------------------

Example:

```json
  {
    "license": "CC-BY-4.0"
  }
```

# SPQR (Scrlo Public Queryable Registration)

## Introduction

SPQR is a public registration table of [Scrlo](https://github.com/neruthes/Scrlo) scripts.

## Principles

- Every Scrlo-compatible script should follow the design specifications as required by Scrlo.
- Every script should be identified by a UUID (lowercase, without hyphens).

## Package Structure

### Package Files

- `spqr.json`
- `index.js`
- `README.md`
- `icon.png`

### File: `spqr.json`

Data fields:

Field			| Description
--------------- | -----------
id              | UUID, lowercase, no hyphens.
name            | Display name of the script.
version         | Version number.
author          | Name of the author.
github_username | GitHub username.
license         | License identifier; similar to the standard in NPM.
homepage        | Homepage of project where the author maintains the script.
match           | Array of RegExp strings; the script will be hidden in the panel if no match found.
auto            | Array of RegExp strings; the script will be executed automatically if any RegExp is matched.

Sample:

```json
{
	"id": "6b747739dc4e4d5ab18bfe7906fafb45",
	"name": "Enhance Wikipedia",
	"version": "1.0.0",
	"author": "Neruthes <neruthes.xyz>",
	"github_username": "neruthes",
	"license": "AGPL-3.0",
	"homepage": "https://github.com/neruthes/jsu",
	"match": [ "\\w{2}\\.wikipedia.org" ],
	"auto": [ "\\w{2}\\.wikipedia.org" ]
}
```

## Contributing

// TODO

## Copyright

Each script has its own copyright declaration.

Documentations are released under [GFDL 1.3](https://www.gnu.org/licenses/fdl-1.3.html).

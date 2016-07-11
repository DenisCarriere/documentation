[![Build Status](https://travis-ci.org/dlcspm/documentation.svg?branch=master)](https://travis-ci.org/dlcspm/documentation)

# DLCSPM Documentation

Preview documentation at [docs.dlcspm.com](https://docs.dlcspm.com).

## Dependencies

You will need to install `Mkdocs` which is a **Python** library & **NodeJS** to run the scripts from the `package.json` using `npm`.

- [Install Python 3.X](https://www.python.org/)
- [Install NodeJS 6.X](https://nodejs.org/en/)

```
$ pip install mkdocs
```

## Publish to Localhost

```bash
$ npm start

> mkdocs serve

INFO    -  Building documentation...
INFO    -  Cleaning site directory
[I 160705 14:00:08 server:281] Serving on http://127.0.0.1:8000
[I 160705 14:00:08 handlers:59] Start watching changes
[I 160705 14:00:08 handlers:61] Start detecting changes
```

Using your favourite web browser open [localhost:8000](localhost:8000).

## Publish to AWS

```bash
$ npm run publish

> dlcspm-docs@1.0.0 publish /Users/mac/Github/cwix
> npm run build && npm run upload

> dlcspm-docs@1.0.0 build /Users/mac/Github/cwix
> mkdocs build --clean

INFO    -  Cleaning site directory
INFO    -  Building documentation to directory: /Users/mac/Github/cwix/site

> dlcspm-docs@1.0.0 upload /Users/mac/Github/cwix
> aws s3 cp ./site s3://docs.dlcspm.com --recursive --acl public-read

upload: {...}
```

## Examples

- https://github.com/linkedin/gobblin

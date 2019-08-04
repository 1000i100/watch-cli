# watch-cli-only [![NPM version](https://badge.fury.io/js/watch-cli-only.svg)](http://badge.fury.io/js/watch-cli-only)

> Command line wrapper for gaze to use in package.json scripts object.

### Install globally

**Install globally with [npm](npmjs.org)**

```bash
npm i -g watch-cli-only
```

## Usage

```bash
watch -p "**/*.js" -c "npm test"
```

### Options

Short | Long | Type | Description
---|---|---|---
`-p` | `--pattern` | `string` | [`glob`](https://github.com/isaacs/node-glob) pattern you are want to watch.
`-c` | `--command` | `string` | Command to execute on watched files change.

### Multi Patterns

It is possible to provide multi paterns, so if one of the files changed, the command will execute.
```
watch -p file1.js -p file2.fs -c command
```

### Exported environment variables

Environment variables available from the command string:

```
FILENAME           Relative filename.
ABSOLUTE_FILENAME  Asolute filename.
EVENT              Event type. Is either 'changed', 'deleted' or 'added'.
```

Use it like this in Linux/macOS:

```
$ watch -p '**/*.js' -c 'jshint $FILENAME'
```

In Windows:

```
> watch -p "**/*.js" -c "jshint %FILENAME%"
```

## Original Author

**Brian Woodward**
 
+ [github/doowb](https://github.com/doowb)
+ [twitter/doowb](http://twitter.com/doowb) 

### New Maintainer

From the old `watch-cli` version to the new `watch-cli-only`

**Millicent Billette**

[1forma-tic.fr](https://1forma-tic.fr)


## License
Copyright (c) 2015 Brian Woodward  
Released under the MIT license

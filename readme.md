# is-heroku-cli

Check if your code is running on Heroku from the command line

[![npm](https://img.shields.io/npm/v/is-heroku-cli.svg?style=flat-square)](https://www.npmjs.com/package/is-heroku-cli)
[![Build Status](https://img.shields.io/travis/seangenabe/is-heroku-cli/master.svg?style=flat-square)](https://travis-ci.org/seangenabe/is-heroku-cli)
[![Dependency Status](https://img.shields.io/david/seangenabe/is-heroku-cli.svg?style=flat-square)](https://david-dm.org/seangenabe/is-heroku-cli)
[![devDependency Status](https://img.shields.io/david/dev/seangenabe/is-heroku-cli.svg?style=flat-square)](https://david-dm.org/seangenabe/is-heroku-cli#info=devDependencies)

## Intro

Just a CLI over [is-heroku](https://www.npmjs.com/package/is-heroku).

## CLI usage

    is-heroku-cli

Returns an exit code of 1 if not running on Heroku.

## Example

You might want to do stuff like a post-install script on Heroku. You can do this
in your package.json:

```json
{
  "scripts": {
    "postinstall": "is-heroku-cli && do-some-stuff || exit 0"
  }
}
```

The `|| exit 0` part is to signal other scripts that you don't really mind if
the preceding part fails (e.g. if `is-heroku-cli` exits with code 1).

## License

MIT

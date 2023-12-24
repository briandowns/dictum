# dictum

Dictum is an opinionated package manaager for [Dictu](github.com/Dictu-lang/Dictu).

## Usage

**NOTE:** This repository includes an example Dictu module called `slog`. It implements a JSON structured logger.

On startup, Dictum will create a top level module directory if it doesn't exist: `${PWD}/dictu_modules` .

`Dictum` expects modules to be packaged in a directory that has been tar'd and gzip'd with an extension of `.tgz`. 


## Install 

```sh
sudo make install
```

## Examples

Create a module. The command below will create a new module from the given directory name. The result will be the a tar'd and gzip'd file named `<module_name.tgz`.

```sh
dictum create <dir_with_dictu_code>
```

Install a module. You can install a module from the local file system or from Github. Additionally, if you install from Github you can specify a tag to install.

```sh
dictum install <module_name>.tgz
```

```sh
dictum install github.com/briandowns/wanbli
```

```sh
dictum install github.com/briandowns/colorize v0.1.0
```

When uninstalling modules, Dictum will search the user path for the given module.

```sh
dictum uninstall <module_name>
```

Get Informtion on a Module

```sh
dictum info <module_name>
```

### Config

You can provide additional config to `dictum` by setting a couple environment variables, `DICTUM_HTTP_TIMEOUT` and `DICTUM_HTTP_INSECURE`. These will be used when making calls to Github.

## Contact

Brian Downs [@bdowns328](http://twitter.com/bdowns328)

## License

dictum source code is available under the BSD 3 Clause [License](/LICENSE).


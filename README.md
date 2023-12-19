# dictum

Dictum is an opinionated package manaager for [Dictu](github.com/Dictu-lang/Dictu).

## Usage

**NOTE:** This repository includes an example Dictu module called `slog`. It implements a JSON structured logger.

On startup, Dictum will create a top level module directory if it doesn't exist: `${PWD}/dictu_modules` .

`Dictum` expects modules to be packaged in a directory that has been tar'd and gzip'd with an extension of `.tgz`. 

### Examples 

Install a module. 

```cs
dictum install <module_name>.tgz
```

When uninstalling modules, Dictum will search the user path for the given module.

```cs
dictum uninstall <module_name>
```

Get Informtion on a Module

```cs
dictum info <module_name>
```

## Future Considerations

* Dependency management
* Manage updates/upgrades
* Pull remote modues

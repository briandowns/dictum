# dictum

Dictum is a POC package manaager for [Dictu](github.com/Dictu-lang/Dictu).

## Usage

This is still a very simple implementation and makes a few naive assumptions, one being that the module to be installed is a directory in the current working directory. 

This repository includes an example Dictu module called `slog`. It implements a JSON structured logger.

On startup, Dictum will create top level module directories if they don't exist. For user modules, the `.dictu` is created in the user's home directory. Modules installed at the system level are installed to `/usr/local/lib/dictu`.

### Examples 

Install a module for the current user. 

```cs
dictum install slog
```

Install a module system-wide.

```cs
dictum install -g slog
```

When uninstalling modules, Dictum will search the user path and system module path for the given module.

```cs
dictum uninstall slog
```

## Future Considerations

* Use SQLite to keep track of installation information
* Dependency management
* Call out version conflicts
* Manage updates/upgrades

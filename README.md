DarvinFilemanBundle
=====================
This bundle integrates "darvinstudio/fileman" with Symfony. It allows to easily exchange uploaded files between
 Symfony-based project's instances.

## Installation

1. Install package using Composer:

```shell
$ composer require darvinstudio/darvin-fileman-bundle
```

2. Register bundle in your AppKernel class:

```php
// app/AppKernel.php

public function registerBundles()
{
    $bundles = [
        // ...
        new Darvin\DatabaserBundle\DarvinFilemanBundle(),
        // ...
    ];
}
```

## Usage

### Pull uploaded files

```shell
$ /usr/bin/env php bin/console fileman:pull [-k|--key [KEY]] [-p|--password] [-P|--port [PORT]] [--parameters [PARAMETERS]] [-h|--help] [-q|--quiet] [-v|vv|vvv|--verbose] [-V|--version] [--ansi] [--no-ansi] [-n|--no-interaction] [-e|--env ENV] [--no-debug] [--] <command> <user@host> <project_path_remote> [<project_path_local>]
```

Examples:

```shell
$ /usr/bin/env php bin/console fileman:pull root@example.com www/example.com
$ /usr/bin/env php bin/console fileman:pull -P 123 root@example.com /var/www/example.com
```

### Push uploaded files

```shell
$ /usr/bin/env php bin/console fileman:push [-k|--key [KEY]] [-p|--password] [-P|--port [PORT]] [--parameters [PARAMETERS]] [-h|--help] [-q|--quiet] [-v|vv|vvv|--verbose] [-V|--version] [--ansi] [--no-ansi] [-n|--no-interaction] [-e|--env ENV] [--no-debug] [--] <command> <user@host> <project_path_remote> [<project_path_local>]
```

Examples:

```shell
$ /usr/bin/env php bin/console fileman:push root@example.com www/example.com
$ /usr/bin/env php bin/console fileman:push -P 123 root@example.com /var/www/example.com
```

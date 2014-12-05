# sportdb - sport.db Command Line Tool in Ruby


<!--
[![Build Status](https://secure.travis-ci.org/geraldb/sport.db.ruby.png?branch=master)](http://travis-ci.org/geraldb/sport.db.ruby)
-->

* home  :: [github.com/sportdb/sport.db.ruby](https://github.com/sportdb/sport.db.ruby)
* bugs  :: [github.com/sportdb/sport.db.ruby/issues](https://github.com/sportdb/sport.db.ruby/issues)
* gem   :: [rubygems.org/gems/sportdb](https://rubygems.org/gems/sportdb)
* rdoc  :: [rubydoc.info/gems/sportdb](http://rubydoc.info/gems/sportdb)
* forum :: [groups.google.com/group/opensport](https://groups.google.com/group/opensport)


## Usage

The sportdb gem lets you load fixtures in plain text into your sports database

~~~
SYNOPSIS
    sportdb [global options] command [command options] [arguments...]

VERSION
    1.8

GLOBAL OPTIONS
    -d, --dbpath=PATH - Database path (default: .)
    -n, --dbname=NAME - Database name (default: sport.db)
    --verbose         - (Debug) Show debug messages
    --version         - Show version

COMMANDS
    create        - Create DB schema
    setup, s      - Create DB schema 'n' load all world and sports data
    update, up, u - Update all sports data
    load, l       - Load sports fixtures
    logs          - Show logs
    props         - Show props
    pull          - Pull (auto-update) event fixtures from upstream sources  
    serve, server - Start web service (HTTP JSON API)
    stats         - Show stats
    test          - (Debug) Test command suite
    help          - Shows a list of commands or help for one command
~~~


### `setup` Command

~~~
NAME
    setup - Create DB schema 'n' load all world and sports data

SYNOPSIS
    sportdb [global options] setup [command options] NAME

COMMAND OPTIONS
    -i, --include=PATH  - Sports data path (default: .)
    --worldinclude=PATH - World data path (default: none)

EXAMPLES
    sportdb setup --include ./at-austria --worldinclude ./world.db
    sportdb setup 2013_14 --include ./at-austria --worldinclude ./world.db
~~~


### `update` Command

~~~
NAME
    update - Update all sports data

SYNOPSIS
    sportdb [global options] update [command options] NAME

COMMAND OPTIONS
    --delete           - Delete all sports data records
    -i, --include=PATH - Sports data path (default: .)

EXAMPLES
    sportdb update --include ./at-austria
    sportdb update --include ./at-austria --delete
    sportdb update 2013_14 --include ./at-austria --delete
~~~

### `load` Command

~~~
NAME
    load - Load sports fixtures

SYNOPSIS
    sportdb [global options] load [command options] NAME

COMMAND OPTIONS
    --delete - Delete all sports data records

EXAMPLES
    sportdb load --include ./at-austria 2013_14/bl
    sportdb load --include ./at-austria 2013_14/bl 2013_14/cup
~~~


### `pull` Command

~~~
NAME
    pull - Pull (auto-update) event fixtures from upstream sources

SYNOPSIS
    sportdb [global options] pull

EXAMPLES
    sportdb pull
~~~


### `serve` Command

~~~
NAME
    serve - Start web service (HTTP JSON API)

SYNOPSIS
    sportdb [global options] serve 

EXAMPLES
    sportdb serve
~~~


## Install

Just install the gem:

    $ gem install sportdb


## Free Open Public Domain Datasets

- [`football.db`](https://github.com/openfootball) - free open public domain football (soccer) data for use in any (programming) language
- [`formula1.db`](https://github.com/opensport/formula1.db) - free open public domain Formula 1/Formula One data for use in any (programming) language
- [`ski.db`](https://github.com/opensport/ski.db) - free open public domain Ski Alpin/Alpine Ski data for use in any (programming) language
- [`american-football.db`](https://github.com/opensport/american-football.db) - free open public domain American Football data for use in any (programming) language


## License

The `sportdb` scripts are dedicated to the public domain.
Use it as you please with no restrictions whatsoever.


## Questions? Comments?

Send them along to the
[Open Sports & Friends Forum/Mailing List](http://groups.google.com/group/opensport).
Thanks!


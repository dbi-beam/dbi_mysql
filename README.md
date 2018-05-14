DBI for Erlang (MySQL)
=======================

[![Build Status](https://api.travis-ci.org/dbi-beam/dbi_mysql.png)](https://travis-ci.org/dbi-beam/dbi_mysql)
[![Codecov](https://img.shields.io/codecov/c/github/dbi-beam/dbi_mysql.svg)](https://codecov.io/gh/dbi-beam/dbi_mysql)
[![License: LGPL 2.1](https://img.shields.io/badge/License-GNU%20Lesser%20General%20Public%20License%20v2.1-blue.svg)](https://raw.githubusercontent.com/dbi-beam/dbi_mysql/master/COPYING)
[![Hex](https://img.shields.io/hexpm/v/dbi_mysql.svg)](https://hex.pm/packages/dbi_mysql)

Database Interface for Erlang and Elixir using SQLite. For further information check [DBI](https://github.com/dbi-beam/dbi).

### Install (rebar3)

To use it, with rebar, you only need to add the dependency to the rebar.config file:

```erlang
{deps, [
    {dbi_mysql, "0.1.0"}
]}
```

### Install (mix)

To use it, with mix, you only need to add the dependency to the mix.exs file:

```elixir
{:dbi_mysql, "~> 0.1.0"}
```

### Configuration

The configuration is made in the configuration file (`sys.config` or `app.config`) so, you can add a new block for config the database connection as follow:

```erlang
{dbi, [
    {mydatabase, [
        {type, mysql},
        {host, "localhost"},
        {user, "root"},
        {pass, "root"},
        {database, "mydatabase"},
        {poolsize, 10}
    ]}
]}
```

In case you're using Elixir, you can define the configuration for your project in this way:

```elixir
confg :dbi, mydatabase: [
              type: :mysql,
              host: 'localhost',
              user: 'root',
              pass: 'root',
              database: 'mydatabase',
              poolsize: 10
```

Enjoy!

---
aliases: 
tags: 
- public
- knowledge
title: Postgresql
date created: "2022-10-10T08:51:08"
date modified: "2022-10-31T07:28:55"
---

# Postgresql

## Errors with Postgresql

See its state with `brew services list`

If postgresql isn't running, start to run postgres with `brew services start postgresql`

If it is running, you can try to restart it with `brew services restart postgresql`

If you have recently updated postgresql and nothing works, you may be able to

Maybe, you can find the logs here `/usr/local/var/log/postgresql@14.log` or at a similar path

If you are desperate and don't have valuable data in your database, just delete everything with something like `rm -Rf /usr/local/var/postgres/*` and reinstall with `brew reinstall postgresql`

## Datatypes in with [[Ruby on Rails|Rails]]

### Usual Types

- :binary
- :boolean
- :date
- :datetime
- :decimal
- :float
- :integer
- :primary_key
- :string
- :text
- :time
- :timestamp

### Special Types

- :json / :jsonb
- :hstore
- :array
- :bytea
- :range
- :interval

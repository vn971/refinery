### v0.3.0 (May 2020)

- **Features**:

  - rename Config.get_db_type to Config.db_type, [#95](https://github.com/rust-db/refinery/pull/95)
  - Deprecate migrate_from_config and migrate_from_config_async, instead impl Migrate for Config, [#94](https://github.com/rust-db/refinery/pull/94)
  - Update Runner.run and Runner.run_async return signature, Result<(), Error> -> Result<Report, Error> where report contains applied Migration's, [#92](https://github.com/rust-db/refinery/pull/92)
  - Deprecate AppliedMigration, merge it's functionality into Migration, [#91](https://github.com/rust-db/refinery/pull/91)
  - Add Runner.get_applied_migrations_async method, [#90](https://github.com/rust-db/refinery/pull/90)
  - Add Runner.get_applied_migrations method, [#90](https://github.com/rust-db/refinery/pull/90)
  - Add Runner.get_last_applied_migration_async method, [#90](https://github.com/rust-db/refinery/pull/90)
  - Add Runner.get_last_applied_migration method
  - Add allow migrations to run up until a Target version, [#74](https://github.com/rust-db/refinery/pull/74)
  - Update mysql_async dependency, 0.21 -> 0.23 [#94](https://github.com/rust-db/refinery/pull/94/files#diff-c265757db229c3cac93fd2e32bf4da58)
  - Update rusqlite dependency, 0.21 -> 0.23 [#88](https://github.com/rust-db/refinery/pull/88)

### v0.2.1 (February 2020)

- **Bufixes**:
  - Update cfg-if to 0.1.10 to fix backtrace bug [#66](https://github.com/rust-db/refinery/pull/66)

### v0.2.0 (December 2019)

- **Features**:

  - Add `tokio-postgres` driver support [#10](https://github.com/rust-db/refinery/pull/19).
  - Add `mysql_async` driver suport [#22](https://github.com/rust-db/refinery/pull/19).
  - Add `migrate_from_config` function
  - Add `migrate_from_config_async` function
  - Update postgres to version 0.17 [#32](https://github.com/rust-db/refinery/pull/32)
  - Allow refinery_cli to select driver via features [#32](https://github.com/rust-db/refinery/pull/32)

- **Bugfixes**:
  - allow multiple statements in migration files [#10](https://github.com/rust-db/refinery/issues/21)
  - when building refinery_cli with default features, build with rusqlite bundled libsqlite3 [#33](https://github.com/rust-db/refinery/issues/21)
  - rename ConnectionError to just Connection as it is a variant for Error enum, and add its source as as source [#36](https://github.com/rust-db/refinery/issues/36)

- **Dependencies**:
  - update rusqlite dependency, 0.18 -> 0.21 [#26](https://github.com/rust-db/refinery/issues/26)

## v0.1.10 (December 10, 2010)

- Intial release.

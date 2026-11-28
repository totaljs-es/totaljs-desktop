<!-- header -->
<p align="center"><img src="icon.png" width="112" height="112" alt="" /></p>

<h1 align="center">TotalSQL</h1>

<p align="center">PostgreSQL, MySQL, MariaDB, SQL Server and SQLite in one window.</p>

<p align="center">
  <img src="https://img.shields.io/badge/version-0.1.1-9ad959" alt="Version 0.1.1" />
  <img src="https://img.shields.io/badge/status-ready-2ea44f" alt="Status: ready" />
  <img src="https://img.shields.io/badge/systems-macOS%20%C2%B7%20Windows%20%C2%B7%20Linux-0078d4" alt="macOS · Windows · Linux" />
</p>

<h2 align="center" id="download">Download</h2>

<p align="center">
  <b>macOS</b> <a href="https://github.com/totaljs-es/totaljs-desktop/releases/download/totalsql-latest/TotalSQL-mac.dmg">Apple silicon and Intel</a><br>
  <b>Windows</b> <a href="https://github.com/totaljs-es/totaljs-desktop/releases/download/totalsql-latest/TotalSQL-windows-x64-setup.exe">x64</a> · <a href="https://github.com/totaljs-es/totaljs-desktop/releases/download/totalsql-latest/TotalSQL-windows-x64.msi">x64 MSI</a> · <a href="https://github.com/totaljs-es/totaljs-desktop/releases/download/totalsql-latest/TotalSQL-windows-arm64-setup.exe">ARM64</a><br>
  <b>Linux x64</b> <a href="https://github.com/totaljs-es/totaljs-desktop/releases/download/totalsql-latest/TotalSQL-linux-amd64.deb">deb</a> · <a href="https://github.com/totaljs-es/totaljs-desktop/releases/download/totalsql-latest/TotalSQL-linux-x86_64.rpm">rpm</a> · <a href="https://github.com/totaljs-es/totaljs-desktop/releases/download/totalsql-latest/TotalSQL-linux-x86_64.AppImage">AppImage</a><br>
  <b>Linux ARM64</b> <a href="https://github.com/totaljs-es/totaljs-desktop/releases/download/totalsql-latest/TotalSQL-linux-arm64.deb">deb</a> · <a href="https://github.com/totaljs-es/totaljs-desktop/releases/download/totalsql-latest/TotalSQL-linux-aarch64.rpm">rpm</a> · <a href="https://github.com/totaljs-es/totaljs-desktop/releases/download/totalsql-latest/TotalSQL-linux-aarch64.AppImage">AppImage</a>
</p>

<p align="center">On a Mac with <a href="https://brew.sh">Homebrew</a>: <code>brew trust totaljs-es/tap &amp;&amp; brew install --cask totaljs-es/tap/totalsql</code></p>
<!-- /header -->

TotalSQL is a client for SQL databases: PostgreSQL, MySQL, MariaDB, SQL Server and SQLite in one window, to read and change their rows, their structure and everything else they hold.

## What it does

- **Connections.** Save your databases in groups, each with the mark of its kind and its environment shown by shape and colour. Several can be open at once, each with its own tabs.
- **Rows.** A table a page at a time, with filters, sorting and the count of rows. Columns move and take the width you give them, and each table remembers it.
- **Changes you review.** Values, new rows and deletions wait in the grid until you read their SQL and save them together. A value is edited by its type: a choice for yes or no, a calendar for dates, checked JSON.
- **The row on the side.** Every value of the selected row whole, to read and to edit.
- **Structure.** Columns, indexes, relations and rules of a table, added, changed and dropped from the window. Each change shows the SQL of its database before it runs.
- **Queries.** A SQL editor with the dialect of the database and its table names. It runs the selection or everything, says what each statement did, and a running statement can be stopped. Each connection keeps its history and its saved queries.
- **Besides tables.** Functions, procedures, sequences, types, triggers, events, extensions and roles, each with the SQL that makes it, as far as each database has them.
- **Export.** A table with its filters, or a result, to CSV, CSV for Excel, JSON or INSERT statements.

## Care

- **A care level for each connection.** Ask before any change (the default), run as written, or read-only.
- **Encrypted connections.** The certificate of the server is checked, and a database behind an SSH server is reached through a tunnel whose key you trust first.
- **Passwords.** Kept in the keychain of your system.

## Copies of a database

TotalSQL writes a whole database to a SQL file that makes it again, with nothing else to install, for the five kinds of database. The file holds the tables in the order of their relations, their rows and their counters, the views, and what you choose of its extensions, types, sequences, functions, procedures, triggers and events. To restore it, open the file in a query of an empty database and run it.

Roles and permissions belong to the server and are not written.

### PostgreSQL images with pg_dump

For PostgreSQL, TotalSQL can also write the copy with `pg_dump`, the tool of PostgreSQL itself. It adds the permissions, takes the whole database at one instant, and can write the compressed archive that `pg_restore` reads (`.dump`), which restores the whole database or only some of its tables.

`pg_dump` is not part of TotalSQL: it uses the one on your computer. To install it:

| System | How |
| --- | --- |
| macOS | With [Homebrew](https://brew.sh): `brew install libpq`. [Postgres.app](https://postgresapp.com) and the installer of [postgresql.org](https://www.postgresql.org/download/macosx/) bring it too. |
| Windows | The installer of [postgresql.org](https://www.postgresql.org/download/windows/). Choosing only "Command Line Tools" is enough. |
| Debian, Ubuntu | `sudo apt install postgresql-client` |
| Fedora, RHEL | `sudo dnf install postgresql` |

There is nothing to set up after that. TotalSQL looks for `pg_dump` in the usual places and, if there are several, uses the newest. Open "Export the database" on a PostgreSQL connection and choose what to write: the SQL file by TotalSQL, the SQL file by `pg_dump` or the archive for `pg_restore`.

`pg_dump` must be of the same version as the server or newer. With an older one, TotalSQL says so and the copy by TotalSQL still works.

## Connect an AI

TotalSQL has an MCP server for an assistant on this computer. It is off until you turn it on, listens only on this computer and asks for a token kept in the keychain. The assistant reads the database in view; a statement that changes anything runs only if you allowed changes, and after your yes in the window. A JavaScript client with a function per tool lets an agent write one script instead of many calls.

## Privacy

TotalSQL talks only to the databases you add. Passwords are kept in the keychain of your system and nowhere else. Nothing is collected about you.

## Report a problem

[Open an issue](https://github.com/totaljs-es/totaljs-desktop/issues/new/choose) and choose TotalSQL, with its version, your system and the kind of database.

# Aegis (Escanor) changelog

All notable changes to this project will be documented in this file.

## [1.6.0] - 2022-02

### Fixed

#### User related stuff

- Fixed Geyser issue
- Fixed a bug where you couldn't join and also not receive an error message

### Changed

- Changed Geyser section in config (enable skip-drop to make Aegis work with Geyser)

## [1.6.0] - 2022-01

### Fixed

#### User related stuff

- Fixed Geyser-support

## [1.5.0] - 2021-12

### Added

#### User related stuff

- Added 1.18 support

## [1.4.1] - 2021-08

### Added

#### User related stuff

- Fixed Geyser support

## [1.4.0] - 2021-08

### Added

#### User related stuff

- Cleaned up much code
- Added geyser support - you have to regenerate your config and enable the support
- Removed some useless command aliases
- Improved bot-handling
- Implemented FastMath
- Implemented FastUtil
- Updated whole [BungeeCord](https://github.com/SpigotMC/BungeeCord) - all new changes are applied
- Updated all dependencies
- Added LibraryLoading feature
- Support from Java 8 to Java 17-ea (Java 11 & 16 are the most stable ones)
- Updated [BotFilter](https://github.com/Leymooo/BungeeCord) - all new changes are applied
- Improved overall performance
- Added blacklist name feature like in normal aegis
- Greatly improved ColouredWriter [@Outfluencer](https://github.com/SpigotMC/BungeeCord/pull/3164)

#### Developer related stuff

- Fixed SLF4J logger
- Fixed Java CI with Maven
    - Improved Java CI with Maven cache

### Changed

- Fixed some typos
- Fixed some wrong prefixes
- Fixed LuckPerms issues
- Fixed general plugin incompatibilities
- Fixed Redis issues
- Fixed BungeeTask issues
- Re-did some messages

### Removed

- Some useless checks

# Aegis Escanor changelog

All notable changes to this project will be documented in this file.


## [2.0.1] - 2023-08

[//]: # (![Ver]&#40;https://img.shields.io/badge/2022--12-1.8.8-f52486?style=for-the-badge&#41;)


![Added](https://img.shields.io/badge/-➕_Added-38b000?style=for-the-badge)

> ![User_stuff](https://img.shields.io/badge/-User_stuff-ff7b00?style=flat-square)

- Added bypass-protocols to config - all version in the list will bypass the fall & drop check
- Added max-handshake-length to config
- BungeeCord & BotFilter Upstream

![Fixed](https://img.shields.io/badge/-❗_Fixed-0466c8?style=for-the-badge)
- Fixed rare-case scenario where you couldn't join the server (Handshake)
- Fixed exception during blacklist file creation

## [2.0] - 2023-07 (Changelog will be adjusted, this is not everything!!)

[//]: # (![Ver]&#40;https://img.shields.io/badge/2023--07-2.0.0-f52486?style=for-the-badge&#41;)

![WIP](https://img.shields.io/badge/-🚧_WIP-3a0ca3?style=for-the-badge)

- Recoded whole Auth-System

![Added](https://img.shields.io/badge/-➕_Added-38b000?style=for-the-badge)

> ![User_stuff](https://img.shields.io/badge/-User_stuff-ff7b00?style=flat-square)

- Added an auto-check for font-manager
- Finished new available bot captcha & drop checks
  - Added new types
    - -1 - disables the check
    - 0 - only checks with the drop check
    - 1 - only checks with captcha
    - 2 - checks drop & captcha
    - 3 - checks for drop, if it fails, then captcha
    - 4 - only checks if CPS is greater than x -> checks for drop, if it fails, then captcha
- Added clean-console
- Added blacklist-feature
  - Way better handling of bots
  - 30K proxies will be downloaded by default
  - Reduced CPU usage by a lot
  - Added config option that lets you decide, whether you want to blacklist invalid protocol versions
- Added `/aegis stats`-command for console
- Added 2 more placeholders to `/aegis`-command
  - {CPU-USAGE}
  - {RAM-USAGE}
- Added 2 new commands
  - `/aegis blacklist <ip>`
  - `/aegis unblacklist <ip>`
- Added few new permissions
  - aegis.command
  - aegis.reload
  - aegis.stats
  - aegis.protection
  - aegis.whitelist
  - aegis.unwhitelist
  - aegis.blacklist
  - aegis.unblacklist
  - aegis.export
- Added the possibility to cancel the PlayerHandshakeEvent [@linsaftw](https://github.com/2lstudios-mc/FlameCord)
- Much faster and better checking for invalid packets
- Applied all [Waterfall](https://github.com/PaperMC/Waterfall) patches
- Added 1.7.x support thanks to [Travertine](https://github.com/PaperMC/Travertine)
  - 1.7.x players are ignored in fall-/ and captcha checks, and we may not support them in the future anymore
- Added the possibility to change F3-Name
- Added new config entries, where you can make your own captcha-pattern & decide the length of the captcha code itself
- Improved captcha generation
  - The console will no longer be frozen until it is finished
- Finished old Aegis antibot-shells
- Added an option where you can change the fall-duration for the fall check
- Added full Geyser-/ and TCP-Shield support
- Added  more database providers: MySQL, H2 and MongoDB
  - We also dropped SQLite support - it's slower than H2 and simple not needed any longer
- Added custom Netty checks which also blocks many bot attacks
- Updated all dependencies
- Changed `aegis.command` permission to `aegis.use`
  - `aegis.<command>` still exists, but it was confusing to have `aegis.command` and `aegis.<command>` as permissions

> ![DEV](https://img.shields.io/badge/-Dev_Stuff-2b9348?style=flat-square)

- Added an API
  - AttackDetectedEvent(EscanorProxyStatistics statistics, AttackType type)
  - BotFilterPassedEvent(String address)
  - CheckFailedEvent(String playerName, String hostAddress, String failed)
  - EscanorProxyStatistics
  - EscanorUtil
    - $underAttack
    - $botCounter

![Fixed](https://img.shields.io/badge/-❗_Fixed-0466c8?style=for-the-badge)

- Fixed BungeeCord modules were not downloaded automatically
  - You must have the following packages installed for this to work:
    - git
    - wget
- Fixed (kinda) JDK 16.0.1 & 16.0.2 support
  - An information message will be sent to the console, simply follow the steps shown
- Fixed ByteBuf memory leaks [@linsaftw](https://github.com/2lstudios-mc/FlameCord)
- Fixed getting kicked if message is too long
- Fixed force enable protection - from command - not working properly
- Fixed always check from config not working properly
- Fixed wrong permissions in whitelist-command & wrong messages
- Fixed Geyser options in config not working properly
- Fixed NullPointerException in PlayerHandshakeEvent from PendingConnection-Class
- Fixed `always-check` option did not work properly
- Fixed TCP-Shield (and other services like this) support
- Fixed rare `NullPointerException` when whitelisting a player after he passed all checks and the IP was null
- Fixed rare `NullPointerException` if disconnect message was null
- Fixed rare `NullPointerException` if the encoder-pipeline was null somehow
- Fixed empty `LoginRequest` data which some botting services might want to

![Removed](https://img.shields.io/badge/-➖_Removed-e01e37?style=for-the-badge)

- Removed redundant name pattern check
- Removed useless `Thread.sleep` for captcha generation
- Removed useless GC call in captcha generation
- Removed never used `SimpleConnector` class
- Removed `fix-scoreboards` and `fix-scoreboard-teams` as you should fix it on your own

![Helpers](https://img.shields.io/badge/-✨_Helpers-3a0ca3?style=for-the-badge)

- A big thank you to all the beta testers who tested the resource with me and reported issues
  - .aniket
  - Dog#2394
  - kokos555
  - marlon#1000
  - Suspect#1234
  - WilliDieEnte
  - Haoshoku#1507
  - XF24XF#7992 (bot-testing)
  - xIsm4 (bot-testing)
  - Louis.rds (Obfuscation config)
  - Ghast [terminalsin] (Obfuscation - Skidfuscator)
- Also, a big thanks to the guys who provided great bot services for testing purposes
  - Arvizzu#1001
  - [McDown](https://mcdown.pw/)
    - Now they have stopped their services, but I have tested a lot with it


[//]: # (![Helpers]&#40;https://img.shields.io/badge/-✨_Helpers-3a0ca3?style=for-the-badge&#41;)

[//]: # ()
[//]: # ()
[//]: # (![Fixed]&#40;https://img.shields.io/badge/-❗_Fixed-0466c8?style=for-the-badge&#41;)

[//]: # ()
[//]: # (![Changed]&#40;https://img.shields.io/badge/-❗_Changed-ffeb3b?style=for-the-badge&#41;)

[//]: # ()
[//]: # (> ![DEV]&#40;https://img.shields.io/badge/-Dev_Stuff-2b9348?style=flat-square&#41;)

[//]: # ()
[//]: # ()
[//]: # (![Added]&#40;https://img.shields.io/badge/-➕_Added-38b000?style=for-the-badge&#41;)

[//]: # ()
[//]: # (![Removed]&#40;https://img.shields.io/badge/-➖_Removed-e01e37?style=for-the-badge&#41;)

[//]: # ()
[//]: # (> ![User_stuff]&#40;https://img.shields.io/badge/-User_stuff-ff7b00?style=flat-square&#41;)

[//]: # ()
[//]: # ()
[//]: # (![Ver]&#40;https://img.shields.io/badge/2022--12-1.8.8-f52486?style=for-the-badge&#41;)

[//]: # ()
[//]: # (![WIP]&#40;https://img.shields.io/badge/-🚧_WIP-3a0ca3?style=for-the-badge&#41;)

[//]: # ()
[//]: # (###########################################################################################)

## [1.9.2] - 2023-08

[//]: # (![Ver]&#40;https://img.shields.io/badge/2022--12-1.8.8-f52486?style=for-the-badge&#41;)


![Added](https://img.shields.io/badge/-➕_Added-38b000?style=for-the-badge)

> ![User_stuff](https://img.shields.io/badge/-User_stuff-ff7b00?style=flat-square)

- Added 1.20.x support

## [1.9.1] - 2023-03

[//]: # (![Ver]&#40;https://img.shields.io/badge/2022--12-1.8.8-f52486?style=for-the-badge&#41;)


![Added](https://img.shields.io/badge/-➕_Added-38b000?style=for-the-badge)

> ![User_stuff](https://img.shields.io/badge/-User_stuff-ff7b00?style=flat-square)

- BungeeCord Upstream
- Enabled captcha for 1.19.4
- Fixed errors with older versions (Upstream)

## [1.9.0] - 2023-03

[//]: # (![Ver]&#40;https://img.shields.io/badge/2022--12-1.8.8-f52486?style=for-the-badge&#41;)


![Added](https://img.shields.io/badge/-➕_Added-38b000?style=for-the-badge)

> ![User_stuff](https://img.shields.io/badge/-User_stuff-ff7b00?style=flat-square)

- Added 1.19.4 support
- Skip captcha for 1.19.4 clients (for now)
- BungeeCord Upstream
- Optimized captcha generation (should be faster now)

## [1.8.8] - 2022-12

[//]: # (![Ver]&#40;https://img.shields.io/badge/2022--12-1.8.8-f52486?style=for-the-badge&#41;)


![Added](https://img.shields.io/badge/-➕_Added-38b000?style=for-the-badge)

> ![User_stuff](https://img.shields.io/badge/-User_stuff-ff7b00?style=flat-square)

- Fixed NullPointerException

## [1.8.7] - 2022-12

[//]: # (![Ver]&#40;https://img.shields.io/badge/2022--12-1.8.7-f52486?style=for-the-badge&#41;)

![Added](https://img.shields.io/badge/-➕_Added-38b000?style=for-the-badge)

> ![User_stuff](https://img.shields.io/badge/-User_stuff-ff7b00?style=flat-square)

- Added 1.19.3 support 

## [1.8.5] - 2022-08


![Added](https://img.shields.io/badge/-➕_Added-38b000?style=for-the-badge)

> ![User_stuff](https://img.shields.io/badge/-User_stuff-ff7b00?style=flat-square)

- Fixed all known issues

## [1.8.4] - 2022-08


![Added](https://img.shields.io/badge/-➕_Added-38b000?style=for-the-badge)

> ![User_stuff](https://img.shields.io/badge/-User_stuff-ff7b00?style=flat-square)

- Added 1.19.2 support

![Removed](https://img.shields.io/badge/-➖_Removed-e01e37?style=for-the-badge)

> ![User_stuff](https://img.shields.io/badge/-User_stuff-ff7b00?style=flat-square)

- Removed {PING} placeholder during fall-/captcha check 

## [1.8.3] - 2022-08


![Added](https://img.shields.io/badge/-➕_Added-38b000?style=for-the-badge)

> ![User_stuff](https://img.shields.io/badge/-User_stuff-ff7b00?style=flat-square)

- Added 1.19.1 support (skip drop & captcha for now)

## [1.8.2] - 2022-07


![Added](https://img.shields.io/badge/-➕_Added-38b000?style=for-the-badge)

> ![User_stuff](https://img.shields.io/badge/-User_stuff-ff7b00?style=flat-square)

- Fixed an issue where the config messages were not displayed during verification

## [1.8.1] - 2022-07


![Added](https://img.shields.io/badge/-➕_Added-38b000?style=for-the-badge)

> ![User_stuff](https://img.shields.io/badge/-User_stuff-ff7b00?style=flat-square)

- Fixed 1.19 support
- Added mc-brand to config (change F3 text)

## [1.8.0] - 2022-07


![Added](https://img.shields.io/badge/-➕_Added-38b000?style=for-the-badge)

> ![User_stuff](https://img.shields.io/badge/-User_stuff-ff7b00?style=flat-square)

- Added 1.19 support
- Added clean-console option to config to stop spamming "favicon" message
- Added session-url to config

## [1.7.3] - 2022-03


![Added](https://img.shields.io/badge/-➕_Added-38b000?style=for-the-badge)

> ![User_stuff](https://img.shields.io/badge/-User_stuff-ff7b00?style=flat-square)

- Invalid first/second login packets can now be configured manually in the config

## [1.7.2] - 2022-03

![Changed](https://img.shields.io/badge/-❗_Changed-ffeb3b?style=for-the-badge)

> ![User_stuff](https://img.shields.io/badge/-User_stuff-ff7b00?style=flat-square)

- Fixed 1.18.2 support
- Updated all dependencies and removed FastUtil

## [1.7.1] - 2022-02

![Changed](https://img.shields.io/badge/-❗_Changed-ffeb3b?style=for-the-badge)

> ![User_stuff](https://img.shields.io/badge/-User_stuff-ff7b00?style=flat-square)

- 1.18.2 player bypass captcha and drop check for now until this error is getting fixed

## [1.7.0] - 2022-02


![Added](https://img.shields.io/badge/-➕_Added-38b000?style=for-the-badge)

> ![User_stuff](https://img.shields.io/badge/-User_stuff-ff7b00?style=flat-square)

- Added 1.18.2 support
- Allow `-` and `.` in online mode as some accounts still have these usernames

## [1.6.1] - 2022-02

![Fixed](https://img.shields.io/badge/-❗_Fixed-0466c8?style=for-the-badge)

> ![User_stuff](https://img.shields.io/badge/-User_stuff-ff7b00?style=flat-square)

- Fixed Geyser issue
- Fixed a bug where you couldn't join and also not receive an error message

![Changed](https://img.shields.io/badge/-❗_Changed-ffeb3b?style=for-the-badge)

- Changed Geyser section in config (enable skip-drop to make Aegis work with Geyser)

## [1.6.0] - 2022-01

![Fixed](https://img.shields.io/badge/-❗_Fixed-0466c8?style=for-the-badge)

> ![User_stuff](https://img.shields.io/badge/-User_stuff-ff7b00?style=flat-square)

- Fixed Geyser-support

## [1.5.0] - 2021-12


![Added](https://img.shields.io/badge/-➕_Added-38b000?style=for-the-badge)

> ![User_stuff](https://img.shields.io/badge/-User_stuff-ff7b00?style=flat-square)

- Added 1.18 support

## [1.4.1] - 2021-08


![Added](https://img.shields.io/badge/-➕_Added-38b000?style=for-the-badge)

> ![User_stuff](https://img.shields.io/badge/-User_stuff-ff7b00?style=flat-square)

- Fixed Geyser support

## [1.4.0] - 2021-08


![Added](https://img.shields.io/badge/-➕_Added-38b000?style=for-the-badge)

> ![User_stuff](https://img.shields.io/badge/-User_stuff-ff7b00?style=flat-square)

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

> ![DEV](https://img.shields.io/badge/-Dev_Stuff-2b9348?style=flat-square)

- Fixed SLF4J logger
- Fixed Java CI with Maven
    - Improved Java CI with Maven cache

![Changed](https://img.shields.io/badge/-❗_Changed-ffeb3b?style=for-the-badge)

- Fixed some typos
- Fixed some wrong prefixes
- Fixed LuckPerms issues
- Fixed general plugin incompatibilities
- Fixed Redis issues
- Fixed BungeeTask issues
- Re-did some messages

![Removed](https://img.shields.io/badge/-➖_Removed-e01e37?style=for-the-badge)

- Some useless checks

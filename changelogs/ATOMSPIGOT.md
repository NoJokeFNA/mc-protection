# AtomSpigot changelog

### 1.4.0 beta
**Important -** For the people who use AtomSpigot as a dependency in their plugin please add `AtomLibs` which is in your server/lib folder.
- Huge Optimization reduced AtomSpigot Jar [From 55.000ko to 5.744ko]
- Fixed MySQL Bug
- Optimized TileEntitySign
- Added LATEST Log4j
- Added Leaves Decay Event [Enable/Disable]
- Added Hide IPs in Console [Enable/Disable]
- Added Enable ProtocolLib [Enable/Disable]
- Added Snowball Particles Options [Enable/Disable]
- Added Better Enchantment [Optimization]

### 1.3.0 beta
- Update - Ticks [You can put a number in it default is 150 on AtomSpigot]
- Optimized Hoppers
- Optimize Printer [Enable / Disable]
- Added Movement Optimization [Enable / Disable]
- Async Catcher [Enable / Disable]
- Pledge Anticheat Packets / with the Pledge info command [Enable / Disable] (Credits to Thomas)
- Server Name Option [AtomSpigot is the default name]
- Enable FastMath [FastMath or NormalMath]
- Lava To Cobble Option [Enable / Disable]
- Player Move Event [Enable / Disable]
- Disable Physics Place [Enable / Disable]
- Added Custom Packets with a PacketHandler and MovementHandler
- Enable ViaVersion [Enable / Disable] [Enable 1.8 - 1.18]
- Enable ViaRewind [Enable / Disable] [Enable 1.7x]
- Fixed Log4j Issue
- Use ASM for Event Executors
- Added Call Helper for Events 

### 1.2.9 beta
- Fixed some issues

### 1.2.8 beta
- Changed "new gen" knockback presets
- Reverted netty update (causes issues with some plugins)
- Spigot no longer compatible with Java 16 (please wait for next update)
- Added bow knockback values
- Fixed error in console with FastAsyncWorldEdit

### 1.2.7 beta
- Added some patches from SportPaper (Related to chunks)
- Re-coded custom grow ticks
- Added knockback preset (kohi, lunar, new generation):
  - Usage: /kb apply-preset <knockback> <lunar:kohi:newgen>
  - In knockback menu: Shift + Click on the knockback item
- Fixed Knockback profiles not saved after restart
- Fixed knockback command
- Added new value to knockback:
  - NewGen: Disable motX and motZ modifiers for the attacker + it always calculate extra values
- Fixed WTap values on knockback
- Fixed some bugs

### 1.2.6 beta
- Fixed ProtocolLib
- Fixed 1.17.1 logins with ViaVersion
- Fixed TPS drops with citizens

### 1.2.5 beta
- Fixed [Citizens](https://www.spigotmc.org/resources/citizens.13811/)
 
### 1.2.4 beta
- Fixed crashes
- Fixed knockback
- Fixed issues with spawners
- Removed useless features
- Spigot is now compatible with Java 16 (credit to [NachoSpigot](https://github.com/CobbleSword/NachoSpigot) for netty update)
- Added some optimizations
- Updated some libraries for minecraft server
  
### 1.2.2 beta
- Fixed Knockback
- Fixed ticks optimization
- Fixed explosions
  
### 1.1 beta
- Fixed Block places with [ViaVersion](https://www.spigotmc.org/resources/viaversion.19254/)
- Removed async tracker
- Added options to allow large packets (keep this option toggled if you want compatibility with all plugins)
- Fixed issues with [ProtocolLib](https://www.spigotmc.org/resources/protocollib.1997/)
  
### 1.0 beta RECODED
- Recoded literally everything

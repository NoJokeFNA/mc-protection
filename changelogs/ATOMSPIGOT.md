# AtomSpigot changelog

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

# <img src="https://ente.dev/api/images/mc-protection96.webp" width="3%"> <b>Basic security & setup</b>

## <b>❤️‍🔥 Firewall</b>
 - You should use a good firewall that limits PPS & CPS so that bot systems can't reach their full performance.
 - You should also block anything that could bypass the server in any way.
   - Like for example [NullPing](https://www.spigotmc.org/wiki/firewall-guide/).
 - We recommend the use of this firewall: https://github.com/GaetanOff/Firewall-Template
 - If you are using our blacklist-feature, which you can enable in the config, you also have to set up 3 more things.
   - First, you have to install [IPSet](https://confluence.jaytaala.com/display/TKB/Using+ipset+to+block+IP+addresses+-+firewall), you can easily do this by executing: `sudo apt-get install ipset`
     - You can check if it is installed simply by executing: `sudo ipset`
   - After you have successfully installed IPSet, you now have to execute three more commands.
     - `sudo ipset create -! blacklist hash:ip hashsize 15000`
     - `sudo iptables -I INPUT -m set --match-set blacklist src -j DROP`
     - `sudo iptables -I FORWARD -m set --match-set blacklist src -j DROP`
 - If you are using [iptables-persistent](https://www.thomas-krenn.com/en/wiki/Saving_Iptables_Firewall_Rules_Permanently), please follow the steps below.
   - Please don't run this file unless you are sure that you are not deleting important firewall data.
   - After making sure that you don't delete any important firewall data, you can run [this file](https://github.com/GaetanOff/Firewall-Template/blob/master/rules) with the new firewall rules.
     - Check if all your rules got correctly updated: `sudo iptables -S`
   - Now you have to save your current rules so they won't get lost (2 options - choose one of them):
     - First option:
       - `sudo iptables-save  <path-to-file.txt`
       - After you have successfully saved your rules, you just have to apply them: `sudo iptables-apply <path-to-file.txt`
     - Second option:
       - `sudo iptables-save`

<hr>

## <b>⛔ AntiVPN</b>
 - In any case, you should also use an AntiVPN system.
 - This can be used to contain almost all attacks because they simply run over tens of proxies.
 - We recommend the use of this AntiVPN-System:
   - https://www.spigotmc.org/resources/58291/
   - https://www.spigotmc.org/resources/93355/
     - Put the plugin on your lobby servers.
       
<hr>

## <img src="https://ente.dev/api/images/766676779049418762.webp" width="3%"> <b> Aegis</b>
 - With Aegis, you are protected by two basic checks (drop and captcha), which certainly don't bypass all bots, but you have to buy a subscription of 15+ euros - if it's not even false advertising.
 - Through umpteen other checks, as well as logical processors that check if it's a bot, you can also be extra protected again.
 - If you use our captcha feature, you may have to install one package on your system: `sudo apt-get install font-manager`
   - If you face any issues with this, try the following solutions:
     - Install `libfontconfig1` and/or `fontconfig` and/or `libxtst6` to your system: `sudo apt-get install <package-name>`
     - Add `-Djava.awt.headless=true` to your startup flags (`java -Xmx... ... -Djava.awt.headless=true -jar BungeeCord.jar`)
   - If you are using [Pterodactyl](https://pterodactyl.io/), use one of the images provided [here](https://github.com/AktiCube/containers) according to the Java version you would like to use.

<hr>

### Aegis Startup flags
<b>Java >17</b><br>
`java -Xms512M -Xmx512M -XX:+UseG1GC -XX:G1HeapRegionSize=4M -XX:+UnlockExperimentalVMOptions -XX:+ParallelRefProcEnabled -XX:+AlwaysPreTouch -Djava.awt.headless=true --add-opens java.base/java.lang=ALL-UNNAMED --add-opens java.base/java.lang.reflect=ALL-UNNAMED --add-opens java.base/java.lang.invoke=ALL-UNNAMED -jar "Escanor 2.0.jar"`

<b>Java 16</b><br>
`java -Xms512M -Xmx512M -XX:+UseG1GC -XX:G1HeapRegionSize=4M -XX:+UnlockExperimentalVMOptions -XX:+ParallelRefProcEnabled -XX:+AlwaysPreTouch -Djava.awt.headless=true --add-opens=java.base/java.lang.reflect=ALL-UNNAMED --illegal-access=warn -jar "Escanor 2.0.jar"`

<b>Java <16</b><br>
`java -Xms512M -Xmx512M -XX:+UseG1GC -XX:G1HeapRegionSize=4M -XX:+UnlockExperimentalVMOptions -XX:+ParallelRefProcEnabled -XX:+AlwaysPreTouch -Djava.awt.headless=true -jar "Escanor 2.0.jar"`
       
<hr>

 ### LobbySystem - PlaceholderAPI Integration
  - /papi ecloud download bungee
  - /papi ecloud download localtime
  - /papi ecloud download player
  - /papi ecloud download playerlist
  - /papi ecloud download server

<hr>

## <b>❗Disclaimer</b>
### We are not responsible for any damage to your network. You set up everything at your own risk. 

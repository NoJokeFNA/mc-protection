# Basic security

## :fire: Firewall :fire:
> - You should use a good firewall that limits PPS & CPS so that bot systems can't reach their full performance.
> - You should also block anything that could bypass the server in any way.
>   - Like for example [NullPing](https://www.spigotmc.org/wiki/firewall-guide/).
> - We recommend you this firewall here: https://github.com/GaetanOff/Firewall-Template
> - If you are using our blacklist-feature, which you can enable in the config, you also have to set up 3 more things.
>   - First, you have to install [IPSet](https://confluence.jaytaala.com/display/TKB/Using+ipset+to+block+IP+addresses+-+firewall), you can easily do this by executing: `sudo apt-get install ipset`
>     - You can check if it is installed simply by executing: `sudo ipset`
>   - After you have successfully installed IPSet, you now have to execute 3 more commands.
>     - `sudo ipset create -! blacklist hash:ip hashsize 15000`
>     - `sudo iptables -I INPUT -m set --match-set blacklist src -j DROP`
>     - `sudo iptables -I FORWARD -m set --match-set blacklist src -j DROP`
> - If you are using iptables-persistent, please follow the steps below.
>   - First, you have to [remove](https://github.com/GaetanOff/Firewall-Template/blob/master/reset) your old rules.
>     - Check if you all your rules got correctly removed: `sudo iptables -S`.
>     - If it only contains `INPUT ACCEPT`, `FORWARD ACCEPT` & `OUTPUT ACCEPT` rules, you did everything right.
>   - Now you have to [apply](https://github.com/GaetanOff/Firewall-Template/blob/master/rules) the new firewall rules.
>     - Check if you all your rules got correctly updated: `sudo iptables -S`.
>   - Now you have to save your current rules, so they won't get lost: `sudo iptables-save > <directory>/<filename>`.
>   - After you have successfully saved your rules, you just have to apply them: `sudo iptables-apply <directory>/<filename>`.

## :rocket: AntiVPN :rocket:
> - In any case you should also use an AntiVPN system.
> - This can be used to contain almost all attacks, because it simply runs over tens of proxies.
> - We recommend this AntiVPN system: https://www.spigotmc.org/resources/gatekeeper-advanced-antivpn-antiproxy.70895/
>   - Put the plugin on your lobby servers.

## :wrench: Aegis :wrench:
> - With Aegis, you are protected by 2 basic checks (drop + captcha), which don't bypass all bots, but you have to buy a subscription of 15+ Euro - if it's not even false advertisement.
> - Through umpteen other checks, as well as logical processors that check if it's a bot, you can also be extra protected again.

# Disclaimer
We are not responsible for any damage on your network. You set up everything on your own risk.

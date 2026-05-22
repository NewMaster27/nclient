# [ nclient-project-automation ]
[!] Automation/Script of tor as a secure proxy on systemd based linux distros also a process manager in real time(about tor)

[!] Actions: --start, --stop. --restart, --boot-enable, --boot-disable, --myip, --change, --status, --fix, --use-bridges </path/to/bridges> <kind(ex: obfs4, etc.)>, --torrc, --help.

[!] Use: git clone https://github.com/NewMaster27/nclient && cd nclient && chmod +x make_bin.sh && sudo ./make_bin.sh && nclient help

# [EXAMPLE USAGE]
- sudo nclient --myip (this prints your public ipv4 address, also geolocation and isp's info)
- sudo nclient --boot-enable (this enables the script to start on boot, it works as a standard systemd.service located on /etc/systemd/system path)
- sudo nclient start (the main function of the script, it touches every single security config for you, it runs firewall rules (iptables based), blocks 100% ipv6 connections at the kernel level(systcl -w net.ipv6...), starts tor with a hard blocked config of 14,9,5 eyes nations is capable to manage system services that may leak your public ip address and it will alays use your loopback interface in everything tor, iptables does (echo "nameserver 127.0.0.1" | sudo tee /etc/resolv.conf))
- sudo nclient -ub 1 my_obfuscated_bridges.txt obfs4 (this param should be used if you want tor to be hide for your ISP, or, if tor is not even alloed in your country)

[!] In addition: 
- Recommended browsers: falkon, surf, torbrowser, librewolf, mullvad, badwolf.
- Recommended: MAC address constant changing.
- Recommended: Use an aditional proxy: proton, mullvad, etc.
- Change iptables rules if needed, by default script modify this to make your traffic tor only, so: tor is killed=no wifi.

[+] Enjoy it !!

sudo ip route add default via 192.168.2.1
sudo sysctl -w net.ipv4.ip_forward=1
sudo iptables -t nat -A POSTROUTING --out-interface wlp2s0 -j MASQUERADE  
sudo iptables -A FORWARD --in-interface enx00c0ca91b5cb -j ACCEPT
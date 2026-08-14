sudo apt install keyd

sudo systemctl enable --now keyd

kate /etc/keyd/default.conf

[ids]
*

[main]
rightalt = layer(nav)

[nav]
j = left
k = down
i = up
l = right


sudo systemctl restart keyd

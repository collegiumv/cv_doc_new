# Auxiliary Services

The lounge network provides some additional services that do not fit
well in other categories.  These additional services are listed on
this page.

## General Network Access

The lounge wired network is available for use by any CV student.  The
wired network has an average speed of 300 mbit/s, but at times of
lower usage can be substantially faster.  No special configuration is
needed to use the wired network --- just plug in your computer and
configure your network adapter to use DHCP (it's the default).
Ethernet cables are provided on a first-come, first-served basis in
the lounge, and are available in the wooden cabinet on the quiet side.

The lounge wireless network is also available for use by any CV
student.  The network operates on 802.11 G and 802.11 AC in the 2.4
and 5Ghz bands, respectively.  The network uses a non-broadcasting
SSID to not disrupt the CometNet services running elsewhere in the
building.  To connect, manually create a network profile with the SSID
'collegiumv' and the password which may be found in the lounge.  Like
the wired network, your device will have to be registered to receive
service on the network.  A working `wpa_supplicant` fragment is
provided below:

```
network={
        ssid="collegiumv"
        scan_ssid=1
        psk="<wifi password>"
        key_mgmt=WPA-PSK
}

```

A limited set of Lounge services are available on the wired and
wireless networks.  At this time, it is possible to access Lounge web
resources, the general access server, and the print-server from the
lounge network.

## IRC Idle Host

carbon.collegiumv.org is maintained as an IRC idle host where you may
use tools such as `tmux` to remain connected to IRC or Jabber servers
in a persistent fashion.  IRC clients `weechat` and `irssi` are
available.  Connection to carbon can be made using either ssh or mosh
and are authenticated by public key.  To [add a
key](account#authorized-keys) to your account, use the command
`modpubkey` on any workstation in the lounge.  Once you have added a
key you can connect to carbon.  The SSH ed25519 fingerprint is:
`AAAAC3NzaC1lZDI1NTE5AAAAIFnRrlEftR5tf4To/Oq2um2adL/rXsNtJFIxyS2J4de7`.

# Auxiliary Services

The lounge network provides some additional services that do not fit well in other categories.  These additional services are listed on this page.

## General Network Access

The lounge wired network is available for use by any CV student.  The wired network has an average speed of 300 mbit/s, but at times of lower usage can be substantially faster.  No special configuration is needed to use the wired network --- just plug in your computer and configure your network adapter to use DHCP (it's the default).  Ethernet cables are provided on a first-come, first-served basis in the lounge, and are available in the wooden cabinet on the quiet side.

## IRC Idle Host

carbon.collegiumv.org is maintained as an IRC idle host where you may use tools such as `tmux` to remain connected to IRC or Jabber servers in a persistent fashion.  IRC clients `weechat` and `irssi` are available.  Connection to carbon can be made using either ssh or mosh and are authenticated by public key.  To [add a key](account#authorized-keys) to your account, use the command `modpubkey` on any workstation in the lounge.  Once you have added a key you can connect to carbon.  The SSH ed25519 fingerprint is: `AAAAC3NzaC1lZDI1NTE5AAAAIFnRrlEftR5tf4To/Oq2um2adL/rXsNtJFIxyS2J4de7`.

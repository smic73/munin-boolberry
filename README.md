# Munin plugins for Boolberry Core

## Installation & Configuration

1. Copy the `boolb_*` scripts to `/usr/share/munin/plugins` then `sudo chmod 755 boolb_*` and ` ln -s /usr/share/munin/plugins/boolb_* /etc/munin/plugins `

1. If you're using SELinux, don't forget to `chcon` them properly.

1. Configure the plugins by creating with root user a file named `/etc/munin/plugin-conf.d/boolb` with this content:


`[boolb_blockchain_size]
user root`

`[boolb_scratchpad_size]
user root`

`[boolb_p2pstate_size]
user root`
   
   
    Adapt it to your setup and avoid using `root`.

Before install check every script and modify with your correct path. Ex: /home/mickey/.boolb

1. Restart the *munin-node* daemon with `systemctl restart munin-node` or `/etc/init.d/munin-node restart`.

1. Done. You should now start to see a new section *boolb* in your Munin pages with the corresponding graphs.

## License

Released under the GNU General Public License v2

http://www.gnu.org/licenses/gpl-2.0.html

## please Donate if you like this script
## BTC: 1L551kGQVnzjWjrQGjTkadgwR6sBf2wu14
## BBR: @silvo

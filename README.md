# Munin plugins for Boolberry Core

## Installation & Configuration

1. Copy the `boolb_*_*` scripts to `/usr/share/munin/plugins` then ` ln -s /usr/share/munin/plugins/boolb_*_* /etc/munin/plugins `

1. If you're using SELinux, don't forget to `chcon` them properly.

1. Configure the plugins by creating with root user a file named `/etc/munin/plugin-conf.d/boolb` with this content:


[boolb_blockchain_size]
user root

[boolb_scratchpad_size]
user root

[boolb_p2pstate_size]
user root
   
   
    Adapt it to your setup and avoid using `root`.

1. Restart the *munin-node* daemon with `systemctl restart munin-node` or `/etc/init.d/munin-node restart`.

1. Done. You should now start to see a new section *boolb* in your Munin pages with the corresponding graphs.

## License

AGPLv3+


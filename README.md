ZoL-munin-plugin
================

A Munin plugin for monitoring ZFS on Linux


How to configure
================
    cp zfs_stats_ /usr/local/bin/
    ln -s /usr/local/bin/zfs_stats_ /etc/munin/plugins/zfs_stats_l2efficiency
    ln -s /usr/local/bin/zfs_stats_ /etc/munin/plugins/zfs_stats_l2utilization
    ln -s /usr/local/bin/zfs_stats_ /etc/munin/plugins/zfs_stats_cachehitdtype
    ln -s /usr/local/bin/zfs_stats_ /etc/munin/plugins/zfs_stats_cachehitlist
    ln -s /usr/local/bin/zfs_stats_ /etc/munin/plugins/zfs_stats_efficiency

    cat <<EOF >> /etc/munin/plugin-conf.d/munin-node
    [zfs_*]
    user root
    EOF

	/etc/init.d/munin-node restart

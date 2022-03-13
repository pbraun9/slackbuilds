# Slackware Linux package build scripts

DRBD V9

        drbd-kernel
        drbd-utils-preview	-- vs. http://slackbuilds.org/repository/15.0/system/drbd-utils/?search=drbd-utils

XEN

	acpica-preview		-- updated version
				-- vs. https://slackbuilds.org/repository/15.0/development/acpica/

<!--
	libvirt-preview		-- updated version (meson build)
	python3-ninja
	python3-skbuild
	urlgrabber-preview	-- updated version
				-- vs. https://slackbuilds.org/repository/15.0/network/urlgrabber/
-->

	xen-nox			-- no SDL no GTK no FUSE and older xenstore daemon
				-- vs. https://slackbuilds.org/repository/15.0/system/xen/

BOOTING

        syslinux-next		-- newer version, conflicts with base
        ucl-preview		-- updated version
				-- vs. https://slackbuilds.org/repository/15.0/libraries/ucl/

VRRP

	keepalived-preview	-- nftables and libipset re-enabled
				-- vs. http://slackbuilds.org/repository/15.0/network/keepalived/

<!--
Linux-HA [reloaded](https://pub.nethence.com/server/linuxha-oldschool)

	cluster-glue
	heartbeat
	resource-agents
	fence-agents
-->

FILE-SYSTEMS

	libaal			-- UP https://slackbuilds.org/repository/15.0/libraries/libaal/
	ocfs2-tools-preview	-- vs. https://slackbuilds.org/repository/15.0/system/ocfs2-tools/
	partclone-preview	-- reiser4 enabled
				-- vs. https://slackbuilds.org/repository/15.0/system/partclone/
	reiser4progs		-- UP https://slackbuilds.org/repository/15.0/system/reiser4progs/

MISC

	clusterit
	dma			-- UP https://slackbuilds.org/repository/15.0/network/dma/

Binaries for those builds are available [over there](https://lab.nethence.com/slackpkgs/)


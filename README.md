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

REISER4

	libaal			UP/SUBMIT
				https://slackbuilds.org/repository/15.0/libraries/libaal/
	reiser4progs		UP/SUBMIT
				https://slackbuilds.org/repository/15.0/system/reiser4progs/
	partclone		SUBMIT -- reiser4 enabled
				https://slackbuilds.org/repository/15.0/system/partclone/

OTHER FILE-SYSTEMS

	ocfs2-tools-preview	TBD
				https://slackbuilds.org/repository/15.0/system/ocfs2-tools/

MISC

	clusterit		SUBMIT
				TBD https://slackbuilds.org/repository/15.0/system/clusterit/
	dma			UP
				https://slackbuilds.org/repository/15.0/network/dma/

Binaries for those builds are available [over there](https://lab.nethence.com/slackpkgs/)


# Slackbuilds for HA, iSCSI and REISER4

## Status

Compare versions of this repository vs. what's been approved at SBo

	grep VERSION= */*

	for url in \
		https://slackbuilds.org/repository/14.2/system/cluster-glue/ \
		https://slackbuilds.org/repository/14.2/network/dma/ \
		https://slackbuilds.org/repository/14.2/system/fence-agents/ \
		https://slackbuilds.org/repository/14.2/system/heartbeat/ \
		https://slackbuilds.org/repository/14.2/libraries/libaal/ \
		https://slackbuilds.org/repository/14.2/system/reiser4progs/ \
		https://slackbuilds.org/repository/14.2/system/resource-agents/ \
		https://slackbuilds.org/repository/14.2/network/tgt/ \
		; do
		lynx -dump $url | grep ']14\.2'
	done; unset url

Note SYSLINUX v6 was not submitted to SBo as it conflicts with base.

Regarding the Heartbeat package and friends, see [Linux-HA old-school](https://pub.nethence.com/server/linuxha-oldschool).

## TODO

- appy debian [patches to syslinux](https://pub.nethence.com/booting/syslinux-install)


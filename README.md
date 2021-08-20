# Slackware Linux package build scripts

Binaries for those builds [are available](https://lab.nethence.com/slackbuilds/)

## Contents

XEN & booting

	xen-nohvm
	python3-ninja
	python3-skbuild
	ucl
	syslinux-next

Linux-HA [reloaded](https://pub.nethence.com/server/linuxha-oldschool)

	cluster-glue
	resource-agents
	heartbeat
	fence-agents

DRBD v9

	drbd-kernel
	drbd-utils-heartbeat

MISC

	libaal
	reiser4progs
	dma

## Status

Some of those are submitted to SlackBuilds.org.

For the record, here's how to compare versions of this repository vs. what's been approved at SBo

	grep VERSION= */*

<!--
XEN & booting
-->

REISER4

	for url in \
		https://slackbuilds.org/repository/14.2/libraries/libaal/ \
		https://slackbuilds.org/repository/14.2/system/reiser4progs/ \
		https://slackbuilds.org/repository/14.2/network/dma/ \
		; do
		lynx -dump $url | grep ']14\.2'
	done; unset url

Linux-HA reloaded

        for url in \
                https://slackbuilds.org/repository/14.2/system/cluster-glue/ \
                https://slackbuilds.org/repository/14.2/system/resource-agents/ \
                https://slackbuilds.org/repository/14.2/system/heartbeat/ \
                https://slackbuilds.org/repository/14.2/system/fence-agents/ \
                ; do
                lynx -dump $url | grep ']14\.2'
        done; unset url

## Resources

SlackBuilds.org
https://slackbuilds.org/

Writing A SlackBuild Script
https://www.slackwiki.com/Writing_A_SlackBuild_Script

Index of /templates
https://slackbuilds.org/templates/


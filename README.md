# Slackware Linux package build scripts

## Owned packages

clusterit
https://slackbuilds.org/repository/15.0/network/clusterit/

    distributed,shell,distributed shell,pdsh,remote,ansible

dma
https://slackbuilds.org/repository/15.0/network/dma/

    email,smtp,mail,sendmail,null,client,nullclient,null-client,mta,msa,mua

libaal
https://slackbuilds.org/repository/15.0/libraries/libaal/

    reiser,reiserfs,reiser4,libaal,reiser4progs,filesystem,file-system,compression,btrfs,partclone

partclone with reiser4
https://slackbuilds.org/repository/15.0/system/partclone/

    partclone,clone,image,filesystem,file-system,restore,reiser4,btrfs

reiser4progs
https://slackbuilds.org/repository/15.0/system/reiser4progs/

    reiser,reiserfs,reiser4,libaal,reiser4progs,filesystem,file-system,compression,btrfs,partclone

xen-nox no SDL no GTK no FUSE and older xenstore daemon
https://slackbuilds.org/repository/15.0/system/xen-nox/

    xen,kvm,vmm,virtualization,libvirt,cloud,hypervisor

systraq
http://slackbuilds.org/repository/15.0/system/systraq/

    ids,security,aide,monitor,notify

## Previews and patch proposals

drbd-kernel for release KVER
(none)

drbd-utils 9.20.2 version update
http://slackbuilds.org/repository/15.0/system/drbd-utils/
by Mario Preksavec

<!--
keepalived by Marek Wodzinski - re-enable nftables and libipset
http://slackbuilds.org/repository/15.0/network/keepalived/

    ha,high availability,health check,lvs,load balance,vrrp,carp
-->

ocfs2-tools 1.8.7 version update and builds fine on multiprocessor
https://slackbuilds.org/repository/15.0/system/ocfs2-tools/
by Mario Preksavec

sshguard - better init script
http://slackbuilds.org/repository/15.0/network/sshguard/
by Andrzej Telszewski

syslinux-next 6.04-debian conflicts with base
(none)

## Builds

Binaries for those builds are available [over there](https://lab.nethence.com/slackpkgs/)

<!--
	libvirt-preview		-- updated version (meson build)
	python3-ninja
	python3-skbuild
	urlgrabber-preview	-- updated version
				-- vs. https://slackbuilds.org/repository/15.0/network/urlgrabber/

Linux-HA [reloaded](https://pub.nethence.com/server/linuxha-oldschool)

	cluster-glue
	heartbeat
	resource-agents
	fence-agents

    cluster,clusterlabs,linuxha,linux-ha,clusterlabs,HA,high-availability,high availability,fault-tolerance,fault tolerance,load-balancing,load balancing
-->

## Useful links

git://git.slackbuilds.org/slackbuilds.git

https://github.com/SlackBuildsOrg/slackbuilds/

https://slackbuilds.org/pending/

https://slackbuilds.org/ready/


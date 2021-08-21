# Preparing the updated syslinux tarball

the resulting tarball [is available](https://lab.nethence.com/nunux/) and was prepared as follows

	wget https://deb.debian.org/debian/pool/main/s/syslinux/syslinux_6.04~git20190206.bf6db5b4+dfsg1-3.debian.tar.xz
	tar xaf syslinux_6.04~git20190206.bf6db5b4+dfsg1-3.debian.tar.xz

	git clone --recursive git://repo.or.cz/syslinux.git

apply the debian patchen

	cd syslinux/
	for patch in ../debian/patches/*.patch; do
		echo PATCH $patch
		patch -p1 < $patch
		echo
	done; unset patch

<!--
make sure it builds before-hand
-->

grab the shortened commit hash from there

	git log -1 | head -1
	cd ../

e.g. as of Aug 2021

	mv syslinux/ syslinux-05ac953/
	tar czf syslinux-05ac953.tar.gz syslinux-05ac953/

## Acceptance

while possibly getting rid of EFI

	cd syslinux-*/
	mv Makefile Makefile.dist
	sed -r 's/^all_firmware := bios .*/all_firmware := bios/' Makefile.dist > Makefile

eventually attempt to build it right away

	make

clean-up everything and deliver the updated tarball

	rm -rf debian/ syslinux_6.04~git20190206.bf6db5b4+dfsg1-3.debian.tar.xz syslinux-05ac953/
	mv syslinux-05ac953.tar.gz ../slackbuilds/syslinux-next/

## Resources

http://cdn.kernel.org/pub/linux/utils/boot/syslinux/

https://packages.debian.org/unstable/syslinux

https://wiki.syslinux.org/wiki/index.php?title=Development


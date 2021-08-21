# Preparing the XEN and QEMU-XEN source tarballs

the resulting tarballs [are available](https://lab.nethence.com/nunux/) and were prepared as follows

grab the [development](https://xenbits.xen.org/gitweb/?p=xen.git;a=summary) branch

        git clone https://xenbits.xen.org/git-http/xen.git
        cd xen/
        git log -1 | head -1
        rm -rf .git*
        cd ../
        mv xen/ xen-54c9736/
        tar czf xen-54c9736.tar.gz xen-54c9736/
        rm -rf xen-54c9736/

grab the [same](https://xenbits.xen.org/gitweb/?p=qemu-xen.git;a=summary) branch as above but now for qemu-xen

        git clone https://xenbits.xen.org/git-http/qemu-xen.git
        # -b stable-4.15
        cd qemu-xen/

        ls -alF ui/keycodemapdb/
	git submodule update --init ui/keycodemapdb
        #git clone https://gitlab.com/qemu-project/keycodemapdb.git

        ls -alF dtc/
	git submodule update --init dtc
        #git clone https://gitlab.com/qemu-project/dtc.git

        ls -alF meson/
        git submodule update --init meson
        #git clone https://github.com/mesonbuild/meson.git

        ls -alF tests/fp/berkeley-*/
	git submodule update --init tests/fp/berkeley-softfloat-3
	git submodule update --init tests/fp/berkeley-testfloat-3
	#git clone https://git.qemu.org/git/berkeley-softfloat-3.git
	#git clone https://git.qemu.org/git/berkeley-testfloat-3.git

        git log -1 | head -1

	COMMIT=136c34c

	rm -rf .git*
        ./configure --help > ../qemu-xen-$COMMIT.configure-help.txt
        cd ../

        mv qemu-xen/ qemu-xen-$COMMIT/
        tar czf qemu-xen-$COMMIT.tar.gz qemu-xen-$COMMIT/

check that it builds and that no X11-related library is there

        cd qemu-xen-$COMMIT/
        ./configure --enable-xen --target-list=i386-softmmu \
		--localstatedir=/var \
		--disable-kvm \
		--disable-docs \
		--disable-guest-agent \
		--python=python3 \
		--sysconfdir=/etc \
                --audio-drv-list= \
                --disable-slirp \
                --disable-blobs \
                --disable-plugins \
                --disable-gtk \
                --disable-sdl \
                --disable-sdl-image \
                --disable-opengl \
                --disable-capstone \
                --disable-fuse \
                --disable-fuse-lseek \
		--cpu=x86_64

        make
        ldd build/qemu-system-i386 | grep gtk # emtpy
        ldd build/qemu-system-i386 | grep sdl # empty
        ldd build/qemu-system-i386 | grep fuse # empty
        cd ../

if we're good, let's clean-up and deliver the tarball

        rm -rf qemu-xen-$COMMIT/


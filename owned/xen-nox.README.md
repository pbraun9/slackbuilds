# building xen-nox

base system deps

    slackpkg install pixman
    slackpkg install fontconfig

    ls -lF /var/log/packages/pixman*
    ls -lF /var/log/packages/fontconfig*

sbo deps

    sbopkg -r
    sbopkg -i acpica
    sbopkg -i yajl

    ls -lF /var/log/packages/acpica*
    ls -lF /var/log/packages/yajl*

eventually clean-up other flavors

    ls -lF /var/log/packages/*xen*
    removepkg ...

    which xl # empty

build xen-nox either from SBo

    time sbopkg -i xen-nox

--or-- manually from the package source

    cd xen-nox/
    grep ^DOWNLOAD= *info
    wget ...
    time ./xen-nox.SlackBuild


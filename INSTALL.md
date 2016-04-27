# Installation

- [OSX](#osx)
- [Fedora / Red Hat / CentOS — (YUM / RPM)](#fedora--red-hat--centos--yum--rpm)
- [Debian / Ubuntu](#debian--ubuntu)
- [Arch Linux](#arch-linux)
- [Gentoo Linux](#gentoo-linux)
- [Other](#other)

<!-- toc -->

### OSX

**yadm** can be installed using [Homebrew](https://github.com/Homebrew/homebrew).

    brew tap TheLocehiliosan/yadm && brew install yadm

### Fedora / Red Hat / CentOS — (YUM / RPM)

Several yum repositories are on Copr. Follow this link for [repositories and installation instructions](https://copr.fedorainfracloud.org/coprs/thelocehiliosan/yadm/).

### Debian / Ubuntu

**yadm** is currently in the "testing" release of Debian. If you are using the "stable" release, you can still install **yadm** using the following process.

* First, add the following to `/etc/apt/sources.list`

        deb http://ftp.debian.org/debian testing main contrib non-free

* Next, run `apt-get update -y`

* Last, run `apt-get -t testing install yadm`

If you are using the "unstable" or "testing" release of Debian, you should be able to install **yadm** as you normally install software with `apt-get`.

### Arch Linux

**yadm** is available in the Arch User Repos and can be installed with AUR helper or Makepkg

    yaourt -S yadm

### Gentoo Linux

**yadm** is not yet available in the main gentoo portage tree, however an ebuild is available for you to use

    mkdir -p /usr/local/portage/app-admin/yadm
    cd $_
    curl -O 'https://raw.githubusercontent.com/TheLocehiliosan/yadm/master/gentoo/yadm-1.04.ebuild' -O 'https://raw.githubusercontent.com/TheLocehiliosan/yadm/master/gentoo/Manifest'
    emerge -atv app-admin/yadm

If you have not configured portage to use `/usr/local/portage` as your local
repository, you also need to add this to the portage `make.conf`

    echo 'PORTDIR_OVERLAY="/usr/local/portage"' >> /etc/portage/make.conf

### Other

You *can* simply download the **yadm** script and put it into your `$PATH`. Something like this:

    curl -fLo /usr/local/bin/yadm https://github.com/TheLocehiliosan/yadm/raw/master/yadm && chmod a+x /usr/local/bin/yadm


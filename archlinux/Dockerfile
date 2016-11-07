FROM base/archlinux
MAINTAINER Florian Bruhin <me@the-compiler.org>

RUN echo 'Server = http://mirror.de.leaseweb.net/archlinux/$repo/os/$arch' > /etc/pacman.d/mirrorlist
RUN pacman-key --init && pacman-key --populate archlinux && pacman -Sy --noconfirm archlinux-keyring
RUN pacman -S --noconfirm pacman && pacman-db-upgrade

RUN pacman -Suyy --noconfirm \
    git \
    python-tox \
    qt5-base \
    qt5-declarative \
    qt5-webkit \
    qt5-webengine \
    python-pyqt5 \
    xorg-xinit \
    xorg-server-xvfb \
    gdb

RUN echo 'en_US.UTF-8 UTF-8' > /etc/locale.gen && locale-gen
ENV LC_ALL=en_US.UTF-8
ENV LANG=en_US.UTF-8

CMD echo "|/usr/lib/systemd/systemd-coredump %P %u %g %s %t %c %e" > /proc/sys/kernel/core_pattern
    git clone /outside qutebrowser.git && \
    cd qutebrowser.git && \
    tox -e py35 || \
    python3 scripts/dev/get_coredumpctl_traces.py

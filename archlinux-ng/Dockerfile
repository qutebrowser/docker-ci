FROM thecompiler/archlinux
MAINTAINER Florian Bruhin <me@the-compiler.org>

RUN pacman -Suyy --noconfirm \
    git \
    python-tox \
    qt5-base \
    qt5-declarative \
    qt5-webkit-ng \
    python-pyqt5 \
    xorg-xinit \
    xorg-server-xvfb

USER user
WORKDIR /home/user

CMD git clone /outside qutebrowser.git && \
    cd qutebrowser.git && \
    tox -e py36

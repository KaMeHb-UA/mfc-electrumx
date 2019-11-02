FROM archlinux/base

RUN pacman -Suy --noconfirm && \
    pacman -S --noconfirm git gcc python python-setuptools && \
    cd / && \
    git clone https://github.com/Exgibichi/electrumx.git && \
    cd electrumx && \
    git checkout mfc && \
    mkdir -p /var/db/electrumx && \
    rm -rf .git && \
    python setup.py install && \
    pacman -R --noconfirm git gcc python-setuptools && \
    rm -rf /var/cache

ENTRYPOINT /electrumx/electrumx_server

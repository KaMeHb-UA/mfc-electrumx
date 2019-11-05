FROM kamehb/archlinux-yay

RUN yay -Suyy --noconfirm --removemake && \
    yay -S --noconfirm --removemake bash mfcoin-cli-bin && \
    rm -rf /var/cache

WORKDIR /root

ENTRYPOINT log() { sleep 5; tail -f /root/.MFC/debug.log & }; log; mfcoind

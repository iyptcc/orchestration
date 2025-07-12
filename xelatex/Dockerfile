FROM ubuntu:rolling

# Setup
RUN apt-get update && \
    DEBIAN_FRONTEND=noninteractive apt-get install -y locales texlive-xetex texlive-latex-recommended latexmk fontconfig texlive-lang-arabic fonts-noto && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/*

ENV LANG=en_US.UTF-8
RUN locale-gen en_US.UTF-8

# Prepare
COPY . /data/fonts/

RUN mkdir -p /usr/share/fonts/opentype/ssp/
RUN find /data/fonts/ssp/ -name "*.otf" -exec install -m644 {} /usr/share/fonts/opentype/ssp/ \; || return 1

RUN mkdir -p /usr/share/fonts/truetype/noori/
RUN find /data/fonts/noori/ -name "*.ttf" -exec install -m644 {} /usr/share/fonts/truetype/noori/ \; || return 1
RUN fc-cache -f -v

RUN mkdir -p /data/src/

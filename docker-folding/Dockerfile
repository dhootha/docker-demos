# Folding@home
#
# docker run -d rgardler/fah
FROM fedora

RUN dnf update -y

RUN dnf install -y https://fah.stanford.edu/file-releases/public/release/fahclient/centos-5.3-64bit/v7.4/fahclient-7.4.4-1.x86_64.rpm

COPY config.xml /

CMD FAHClient

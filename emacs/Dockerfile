FROM rgardler/revealjs
MAINTAINER Ross Gardler rgardler@apache.org

WORKDIR /revealjs
RUN grunt serve &

RUN mkdir /emacs
WORKDIR /emacs

RUN apt-get update && apt-get install -y emacs24-nox && apt-get clean

ADD ./emacs.el  /.emacs.el
RUN emacs --script /.emacs.el

CMD ["emacs"]
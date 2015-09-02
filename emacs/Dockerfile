FROM rgardler/revealjs
MAINTAINER Ross Gardler rgardler@apache.org

RUN apt-get update && apt-get install -y emacs24-nox && apt-get clean

WORKDIR /revealjs

RUN mkdir /projects
WORKDIR /projects

COPY ./.emacs.el  /projects/.emacs.el
RUN emacs --script /projects/.emacs.el

CMD ["emacs"]

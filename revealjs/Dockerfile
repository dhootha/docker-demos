FROM node

MAINTAINER Ross Gardler <rgardler@apache.org>

RUN git clone https://github.com/hakimel/reveal.js.git /revealjs

WORKDIR /revealjs

RUN npm install -g grunt-cli && npm install
RUN sed -i Gruntfile.js -e 's/port: port,/port: port, hostname: "",/'

EXPOSE 80

COPY slides.html /revealjs/index.html
COPY readme.md /revealjs/slides.md

ONBUILD COPY readme.md /revealjs/slides.md

CMD ["grunt", "serve"]


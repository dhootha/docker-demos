# Docker Driven Presentations

### Ross Gardler
### @rgardler

---

# Docker + Reveal.js

Deliver your presentations from Docker

Use Markdown for slides

This is file provides both a readme and a slide deck

Delivers slides using [reveal.js](https://github.com/hakimel/reveal.js)

## Details

This is a Docker container that provides a web server to
deliver slides to a browser. The slides are written in Markdown (in
fact this readme.md files is a slide deck!).

---

# To use

Create a Dockerfile:

```Dockerfile
FROM rgardler/revealjs
```

---

# Slide Content

By default slides come from readme.md file

```markdown
# This is the first slide

### Author
### Contact Details
```

---

# Notes


'## Details' marks the start of your notes

Content after '## Details' will not appear on slide.

Useful for adding explanatory text to the readme.md


---

The end of a slide is indicated by '---' at the start of a line

--

You can also have "child slides", simply separate this from the "parent
slide" with '--'

---

You can customize the way reveal.js behaves by replacing index.html
with your own version.

See [reveal.js documentation](https://github.com/hakimel/reveal.js)

---

Build your container:

```bash
docker build slides .
```

---

Start your container:

```bash
docker run --rm -p 8000:8000 slides
```

---

Navigate to your deck:

```
http://localhost:8000
```

---

There is much more to reveal.js than this.

[reveal.js documentation](https://github.com/hakimel/reveal.js)

# Enjoy!

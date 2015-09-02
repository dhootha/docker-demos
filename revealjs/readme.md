# Docker Driven Presentations

### Ross Gardler
### @rgardler

---

# Docker + Reveal.js

Deliver your presentations from Docker

Use Markdown for slides

Delivers slides using [reveal.js](https://github.com/hakimel/reveal.js)

## Details

This is a Docker container that provides a web server to
deliver slides to a browser. The slides are written in Markdown (in
fact this readme.md files is a slide deck!).

Start the container with demo content using:

```bash
docker run --rm -p 8000:8000 rgardler/revealjs
```

Now point your browser at http://yourhost:8000

---

# Avoid duplicating content

This is file provides both a readme.md and a slide deck

---

# Using rgardler/revealjs

Create a Dockerfile:

```Dockerfile
FROM rgardler/revealjs
```

---

# Add Slide Content

By default slides come from readme.md file

```markdown
# This is the first slide

### Author
### Contact Details
```

---

# Separating Slides

Slides are separated by '---' at the start of a line

--

# Child Slides

You can also have "child slides"

Transition from the bottom when navigating with 'space'

Can be skipped by navigating with 'right arrow'

Child slides are separated from the "parent
slide" with '--'

---

# Longform Notes

'## Details' marks the start of your notes

Content after '## Details' will not appear on slide.

Useful for adding explanatory text to the readme.md

---

# Customization

Reveal.js is highly customizable

Replace index.html with your own version.

See the [reveal.js documentation](https://github.com/hakimel/reveal.js)

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

---

## Details

### Building rgardler/revealjs

```bash
docker build -t rgardler/revealjs .
```

### Running rgardler/revealjs

```bash
docker run -p 8000:8000 rgardler/revealjs
```


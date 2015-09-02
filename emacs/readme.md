# My Emacs Machine

This demo shows how you might create an Emacs container for working
with text files of various types.

---

# Dockerfile

At this point the Dockerfile is really simple, it just installs emacs.

--

# Slides

FROM rgardler/realjs

Means readme.md files are also slide decks

---

# Running

docker run -it rgardler/emacs

---

# Configuration

Self contained

All configuration and files in Git

---

# Building

docker build rgardler/emacs .

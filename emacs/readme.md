# My Emacs Machine

This demo shows how you might create an Emacs container for working
with text files of various types.

---

# Dockerfile

Install emacs

Add .emacs.el file

Configure emacs using .emacs.el

--

# Slides

FROM rgardler/revealjs

Means readme.md files are also slide decks

FIXME: provide a command to start the revealjs server

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

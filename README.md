# Omnifood — HTML

**Live demo:** (https://a2sn2.github.io/Omnifood-html/)

---

## Table of contents

* [Project goals](#project-goals)
* [File structure](#file-structure)
* [How to view locally](#how-to-view-locally)
* [HTML walkthrough](#html-walkthrough)

  * [Header / Navigation](#header--navigation)
  * [Hero](#hero)
  * [Featured logos](#featured-logos)
  * [How it works](#how-it-works)
  * [Meals](#meals)
  * [Testimonials + Gallery](#testimonials--gallery)
  * [Pricing](#pricing)
  * [Call to Action (form)](#call-to-action-form)
  * [Footer](#footer)
* [Accessibility notes](#accessibility-notes)
* [Next steps (when CSS/JS are allowed)](#next-steps-when-cssjs-are-allowed)

---

## Project goals

* Deliver the page layout.
* Use **semantic tags** (`header`, `nav`, `section`, `article`, `aside`, `footer`).
* Keep content **linkable** with anchor IDs (so the navbar jumps to sections).
* Keep images local under `img/` so deployment is simple.

---

## File structure

```
Omnifood-html/
├─ index.html          
└─ img/                
   ├─ omnifood-logo.png
   ├─ hero.webp
   ├─ customers/...
   ├─ app/...
   ├─ meals/...
   ├─ logos/...
   └─ gallery/...
```

> Note: Favicons are optional, but included via `<link rel="icon">` and `<link rel="apple-touch-icon">`.

---

## How to view locally

1. Clone or download this repo.
2. Open `index.html` directly in your browser (double-click or drag it into a tab).
   No build tools, no server required.

---

## HTML walkthrough

### Header / Navigation

* Uses `<header>` and a `<nav>` with a simple `<ul>`.
* Links point to section IDs (`#how`, `#meals`, `#testimonials`, `#pricing`, `#cta`).
* The Omnifood logo is a plain `<img>` wrapped in an anchor.

### Hero

* Contains the main headline (`<h1>`), supporting paragraph, and two text links:

  * “Start eating well” → `#cta`
  * “Learn more” → `#how`
* Shows a small “Recent customers” strip (images + short stat).
* The main hero image is an `<img>` below the copy.

### Featured logos

* A simple section with heading “As featured in” and 5 logo images.

### How it works

* Section with heading (`<h2>`) and **three** `<article>` elements for the steps.
* Each article includes a step heading (`<h3>`), a short description, and an app screenshot.

### Meals

* A heading and two meal cards as `<article>` elements:

  * Image, meal name (`<h3>`), and bullet list of attributes.
* A short “See all recipes” link (currently points back to the section).
* An `<aside>` lists compatible diets.

### Testimonials + Gallery

* Four `<blockquote>` elements for short quotes + `<cite>` for attribution.
* A 12-image gallery (just a grid of `<img>` tags with concise alt text like “Dish 1”, “Dish 2”, …).

### Pricing

* Two pricing `<article>` blocks (Starter and Complete).
* Each block has a price line and a features `<ul>`.
* A simple link “Start eating well” that scrolls to the CTA section.
* A small feature row of four mini-articles (never cook again, local & organic, no waste, pause).

### Call to Action (form)

* A basic `<form>` with:

  * Name (`<input type="text">`)
  * Email (`<input type="email">`)
  * Source dropdown (`<select>`)
  * Submit button
* No JavaScript validation is added (HTML-only version).

### Footer

* Company logo and copyright.
* Address as a semantic `<address>`.
* Three link columns: Account, Company, Resources.

---

## Accessibility notes

* Landmarks: `header`, `nav`, `section`, `footer` provide structure for screen readers.
* Headings are hierarchical (`h1` → `h2` → `h3`…).
* Images include `alt` text. Decorative images could use empty `alt=""` later when styling is added.
* The nav uses a list and in-page anchors so keyboard users can jump quickly.

---



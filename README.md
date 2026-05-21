# Bento Grid

Frontend Mentor challenge – Bento grid layout built with HTML, CSS, and Bootstrap.

My solution to the [Bento grid](https://www.frontendmentor.io/challenges/bento-grid-RMydElrlOj) on Frontend Mentor.

## Overview

A fully responsive bento-style feature grid with eight cards, built to match the Frontend Mentor design across mobile (320px–425px) and desktop breakpoints.

## Features

- **Responsive layout**: Optimized for 320px, 375px, and 425px mobile screens, with desktop layout from the `lg` breakpoint (992px) upward.
- **Semantic HTML**: Uses `<main>`, `<section>`, and `<article>` for each card, with descriptive `alt` text on images.
- **Bootstrap grid**: Nested `row` / `col` layout with `order` utilities so left-column cards move to the bottom on mobile, matching the design.
- **Equal-height columns**: `flex-lg-fill` and `align-items-stretch` align the left column height with the right column on desktop.
- **Cropped illustrations**: Platform icons, calendar, and schedule chart clip at card edges using `overflow: hidden` and custom media wrappers.
- **Flexible card content**: Schedule card keeps a fixed height while fitting a title, chart, and paragraph below.

## Built With

- **HTML5** (semantic markup)
- **CSS3**
- **Bootstrap 5**
- **Google Fonts** (DM Sans)

## Project Structure

```
├── design/                  # Frontend Mentor design previews/references
├── assets/images/           # Illustration assets
├── css/
│   ├── reset.css            # Base reset styles
│   └── styles.css           # Custom styles, layout, crops, and mobile media queries
├── index.html               # Main page markup and bento grid
├── style-guide.md           # Colors and typography reference

```

## How It Works

- **Desktop layout**
  - Left column (`col-lg-3`): “Create post” and “Write with AI” cards stacked vertically.
  - Right column (`col-lg-9`): Purple hero card, platform/schedule cards, schedule-to-social card, growth stats, and followers card in a nested grid.
  - `gap-3` on flex columns and `g-3` on Bootstrap rows control spacing between cards.

- **Mobile layout**
  - All columns become `col-12` and stack in a single column.
  - `order-1` / `order-2` with `order-lg-0` reorders cards so the purple hero appears first and the left-column cards appear last.
  - Bottom row uses order utilities so “Grow followers” appears before the “>56%” card on small screens.
  - Media queries at 425px, 375px, and 320px (at the bottom of `styles.css`) adjust typography, padding, and image crop values.

- **Cropped images**
  - Wrapper classes (`.card-d__media`, `.card-e__media`, `.card-g__media`) use `overflow: hidden`.
  - Images are sized larger than their containers so content clips naturally at the card edge.

## Design

The designs for this project are provided by Frontend Mentor and are located in the **`/design`** folder. The folder contains desktop and mobile UI references.

Every detail of the design was followed as closely as possible — including layout, typography, spacing, card colours, cropped illustrations, and the mobile card order — using **Bootstrap utilities** combined with **custom CSS**.

## Acknowledgements

- Challenge by **Frontend Mentor**

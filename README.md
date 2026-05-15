# Physics +1: Astronomy

**Author:** Nik Bear Brown
**Series:** Physics +1 (Volume 8)
**Publisher:** Bear Brown, LLC
**Status:** Draft

---

## About this book

*Astronomy as the physics of incomprehensible scale.* This is the eighth volume in the Physics +1 series. Where conventional astronomy texts hand the student facts about objects they will never touch, this book teaches the *machinery of inference* — how we know what a star is, how far away it is, what it is made of, and how it ends, all from light. The narrative arc moves outward in scale: from a single point of light to the solar system, then to stars and their deaths, then to galaxies and the universe-scale structure that emerged from the Big Bang.

The +1 layer is interactive: every chapter is designed around a D3 simulation that supplies the visceral feel of size, time, and dynamics that prose alone cannot — orders-of-magnitude zooms, H–R diagrams the reader can build, gravitational-wave geometries, the cosmic distance ladder with its uncertainties made visible.

Audience: intro-astronomy students and curious readers comfortable with high-school algebra. The 30-chapter set in `chapters/` is the full openstax-derived source; `outline.md` proposes a curated 14-chapter subset for the published volume.

## How this directory is organized

```
book.md              ← one-sentence pitch, argument, gap, reader, high-level outline (planning)
outline.md           ← working TOC with D3 simulation notes per chapter
vision.md            ← Tic TOC Phase 1: vision and positioning
architecture.md      ← Tic TOC Phase 2: learning architecture
chapters-spec.md     ← Tic TOC Phase 3: per-chapter specifications
risks.md             ← Tic TOC Phase 4: scope, comparables, adoption risks
pantry/              ← scratch storage for fragments and snippets
chapters/            ← drafts (this is where the book lives)
images/              ← figures and hero images per chapter
styles/              ← Kindle-bound CSS (shared base + book-specific overrides)
build.sh             ← compile the EPUB
graphs.sh            ← process figure-placeholder comments into images/tables
```

## Detailed Table of Contents

### Front Matter

| File | Section |
|------|---------|
| `chapters/00-frontmatter.md` | Title page, copyright, dedication, preface |
| `chapters/00b-introduction.md` | Book-level introduction (reader's roadmap; "A note about AI" is substantive) |

### Chapters

| # | File | Title |
|---|------|-------|
| 1 | `chapters/01-science-and-the-universe-a-brief-tour.md` | Science and the Universe: A Brief Tour |
| 2 | `chapters/02-observing-the-sky-the-birth-of-astronomy.md` | Observing the Sky: The Birth of Astronomy |
| 3 | `chapters/03-orbits-and-gravity.md` | Orbits and Gravity |
| 4 | `chapters/04-earth-moon-and-sky.md` | The Tilt of Everything: Why Our Seasons Run Backwards |
| 5 | `chapters/05-radiation-and-spectra.md` | Light and Spectra: Reading the Universe from a Distance |
| 6 | `chapters/06-astronomical-instruments.md` | The Instruments Between Us and the Light |
| 7 | `chapters/07-other-worlds-an-introduction-to-the-solar-system.md` | Other Worlds: An Introduction to the Solar System |
| 8 | `chapters/08-earth-as-a-planet.md` | Earth as a Planet |
| 9 | `chapters/09-cratered-worlds.md` | Cratered Worlds: What the Moon and Mercury Tell Us About the Early Solar System |
| 10 | `chapters/10-earthlike-planets-venus-and-mars.md` | Earthlike Planets: Venus and Mars |
| 11 | `chapters/11-the-giant-planets.md` | The Giant Planets: Worlds of Hydrogen and Fire |
| 12 | `chapters/12-rings-moons-and-pluto.md` | Rings, Moons, and Pluto: The Outer System's Architecture |
| 13 | `chapters/13-comets-and-asteroids-debris-of-the-solar-system.md` | Comets and Asteroids: Debris of the Solar System |
| 14 | `chapters/14-cosmic-samples-and-the-origin-of-the-solar-system.md` | Cosmic Samples and the Origin of the Solar System |
| 15 | `chapters/15-the-sun-a-garden-variety-star.md` | The Sun: A Garden-Variety Star |
| 16 | `chapters/16-the-sun-a-nuclear-powerhouse.md` | The Sun Burning: Why Four Billion Years of Light Comes from Turning Mass into Energy |
| 17 | `chapters/17-analyzing-starlight.md` | Analyzing Starlight |
| 18 | `chapters/18-the-stars-a-celestial-census.md` | The Stars: A Celestial Census |
| 19 | `chapters/19-celestial-distances.md` | Measuring the Distance to the Stars |
| 20 | `chapters/20-between-the-stars-gas-and-dust-in-space.md` | Between the Stars: Gas and Dust in Space |
| 21 | `chapters/21-the-birth-of-stars-and-the-discovery-of-planets-outside-the-solar-system.md` | The Birth of Stars and the Discovery of Worlds Beyond |
| 22 | `chapters/22-stars-from-adolescence-to-old-age.md` | Stars: From Adolescence to Old Age |
| 23 | `chapters/23-the-death-of-stars.md` | The Death of Stars |
| 24 | `chapters/24-black-holes-and-curved-spacetime.md` | Black Holes and Curved Spacetime |
| 25 | `chapters/25-the-milky-way-galaxy.md` | The Milky Way Galaxy |
| 26 | `chapters/26-galaxies.md` | Galaxies: Islands in the Dark |
| 27 | `chapters/27-active-galaxies-quasars-and-supermassive-black-holes.md` | Active Galaxies, Quasars, and Supermassive Black Holes |
| 28 | `chapters/28-the-evolution-and-distribution-of-galaxies.md` | The Evolution and Distribution of Galaxies |
| 29 | `chapters/29-the-big-bang.md` | The Universe's First Three Minutes: Evidence for the Beginning |
| 30 | `chapters/30-life-in-the-universe.md` | Life in the Universe |

### Back Matter

| File | Section |
|------|---------|
| `chapters/99-back-matter.md` | Acknowledgments, About the Author, References, Glossary, Errata |

## Build

```bash
./build.sh
```

Output lands in `output/` (gitignored).

## Figures

```bash
./graphs.sh
```

Processes `<!-- → [TYPE: description] -->` comments throughout the chapters:
tabular figures become classed markdown tables; non-tabular figures become
placeholder images in `images/`, ready to replace; CSS log appends to
`styles/kindle-book.css` on each run.

## Publish

Upload `output/physics-plus-one-astronomy.epub` to [KDP](https://kdp.amazon.com).

# Personal Website

This repository hosts the source code for my academic and engineering portfolio (as well as some personal hobbies), hosted via [GitHub Pages](https://pages.github.com/) and powered by [Jekyll](https://jekyllrb.com/).

**Live Site:** 🚧IN PROGRESS🚧

---

## Overview

This website serves as a central hub for my research, publications, and technical projects. Key sections include:

- **Research & Publications:** Summaries of current research projects, preprints, and published papers (with links to PDFs and code).
- **Curriculum Vitae:** An updated overview of my academic background, technical skills, and research experience.
- **Essays:** Long-form (and likely poorly-written) essays exploring the intersection of science/mathematics, philosophy/metaphysics, and ethics.
- **Projects:** Highlighted open-source repositories, hardware/software demos, and engineering side projects.

---

## Tech Stack

- **Site Generator:** [Jekyll](https://jekyllrb.com/)
- **Hosting:** [GitHub Pages](https://pages.github.com/) (Deployed via GitHub Actions)
- **Styling & Assets:** HTML5, CSS3/Sass, Markdown
- **CI/CD:** Automated build and deployment via `.github/workflows/jekyll.yml`

---

## Local Development Setup

To run and preview this site locally on your machine:

### Prerequisites

Install [Pixi](https://pixi.sh/) on your machine:
```bash
curl -fsSL https://pixi.sh/install.sh | bash
```

### Installation & Run

```bash
# Clone the repository
git clone https://github.com/mattdula/mattdula.github.io.git
cd mattdula.github.io

pixi run install     # Install the environment
pixi run serve       # Start the local Jekyll server
```
 Open [http://localhost:4000](http://localhost:4000) to preview changes in real time.

### Managing Dependencies

- **System & Binary Dependencies:** Tracked in [pixi.toml](pixi.toml) (managed via `pixi add <package>`).
- **Ruby Gems & Jekyll Plugins:** Tracked in [Gemfile](Gemfile) (managed via `pixi run bundle add <gem-name>`).

---

## Contact & Connect

- [**Google Scholar**](https://scholar.google.com/citations?user=u0haBbcAAAAJ&hl=en&oi=ao)
- [**LinkedIn**](https://www.linkedin.com/in/matthew-dula)
- [**Email me**](mailto:dulamatt@msu.edu)

## License

The code in this repository is licensed under the [MIT License](LICENSE).

*Content, writing, essays, and original works are ©️Matt Dula unless otherwise noted.*

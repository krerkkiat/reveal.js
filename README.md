<p align="center">
  <a href="https://revealjs.com">
  <img src="https://hakim-static.s3.amazonaws.com/reveal-js/logo/v1/reveal-black-text-sticker.png" alt="reveal.js" width="500">
  </a>
  <br><br>
  <a href="https://github.com/krerkkiat/reveal.js-ou-eecs/actions"><img src="https://github.com/krerkkiat/reveal.js-ou-eecs/workflows/tests/badge.svg"></a>
  <a href="https://slides.com/"><img src="https://s3.amazonaws.com/static.slid.es/images/slides-github-banner-320x40.png?1" alt="Slides" width="160" height="20"></a>
</p>

## The OU EECS Theme

An attempt to replicate the [OU's branded template](https://www.ohio.edu/business/resources/faculty-staff/branded-templates) ([an EECS one](https://docs.google.com/presentation/d/1Fq-n81xTSQ3begtrmfPXXjzjtwUfF-CI/edit?usp=sharing&ouid=102167933025944444522&rtpof=true&sd=true)) in reveal.js. So far the logo on the top left and the college or department name on
the bottom left are implemented.

Why reveal.js? So far it seems to be the most mature and still being maintained. With reveal.js you can
also

- Write your content using Markdown or HTML/CSS.
- Have code with syntax highlighting for free.

### Viewing the Slides

Install the dependencies.

```console
npm install
```

You will also need `jq` and `pandoc` if you want to use the BiBTeX citation.

Start the development server.

```console
npm run bib
npm run start
```

### Features

**Light Background**

In Markdown, add

```markdown
<!-- .slide: data-ou-bg-type="light" -->
```

For HTML, just add that `data-ou-bg-type="light"` to the `<section>` tag.

**References with BibTex**

Put your BibTex entries in `ref.bib` file. To cite the entry,

```markdown
[@name](#/references)
```

The `(#/references)` has to be there since the renderer is hooked into a link token of [marked.js](https://marked.js.org/).

If you want to manually refresh the ref entry, you can run

```console
npm run bib
```

The file `ref.html` and `ref.json` are used, so please check them into the VSC. The `ref.html` is used
to diplay under the reference section (via an `iframe` tag). The `ref.json` is used to determine the correct value
of in-line citation.

To use a different style, get the CSL style sheet from [https://github.com/citation-style-language/styles](https://github.com/citation-style-language/styles), then, for now, you will have to modify the command
in `gulpfile.js`.

Since the conversion is done via `pandoc`, you can use [any format that pandoc supports](https://pandoc.org/MANUAL.html#specifying-bibliographic-data)

**Font**

If you want to have same font as the tempalte, follow the instructions at https://www.ohio.edu/ucm/ohio-brand/typography.

### Want to Modify the Theme?

The source file is at `css/theme/source/ou.scss`. You can then re-build the theme with

```console
npm run build -- css-themes
```

### Known Limitations

- The numbering of the citation is not as it appear on the slide.

---

## About reveal.js

reveal.js is an open source HTML presentation framework. It enables anyone with a web browser to create beautiful presentations for free. Check out the live demo at [revealjs.com](https://revealjs.com/).

The framework comes with a powerful feature set including [nested slides](https://revealjs.com/vertical-slides/), [Markdown support](https://revealjs.com/markdown/), [Auto-Animate](https://revealjs.com/auto-animate/), [PDF export](https://revealjs.com/pdf-export/), [speaker notes](https://revealjs.com/speaker-view/), [LaTeX typesetting](https://revealjs.com/math/), [syntax highlighted code](https://revealjs.com/code/) and an [extensive API](https://revealjs.com/api/).

---

Want to create reveal.js presentation in a graphical editor? Try <https://slides.com>. It's made by the same people behind reveal.js.

---

### Sponsors
Hakim's open source work is supported by <a href="https://github.com/sponsors/hakimel">GitHub sponsors</a>. Special thanks to:
<div align="center">
  <table>
    <td align="center">
      <a href="https://workos.com/?utm_campaign=github_repo&utm_medium=referral&utm_content=revealjs&utm_source=github">
        <div>
          <img src="https://user-images.githubusercontent.com/629429/151508669-efb4c3b3-8fe3-45eb-8e47-e9510b5f0af1.svg" width="290" alt="WorkOS">
        </div>
        <b>Your app, enterprise-ready.</b>
        <div>
          <sub>Start selling to enterprise customers with just a few lines of code. Add Single Sign-On (and more) in minutes instead of months.</sup>
        </div>
      </a>
    </td>
  </table>
</div>

---

### Getting started
- 🚀 [Install reveal.js](https://revealjs.com/installation)
- 👀 [View the demo presentation](https://revealjs.com/demo)
- 📖 [Read the documentation](https://revealjs.com/markup/)
- 🖌 [Try the visual editor for reveal.js at Slides.com](https://slides.com/)
- 🎬 [Watch the reveal.js video course (paid)](https://revealjs.com/course)

--- 
<div align="center">
  MIT licensed | Copyright © 2011-2024 Hakim El Hattab, https://hakim.se
</div>

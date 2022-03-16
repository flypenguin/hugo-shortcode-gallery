# Image galleries

The gallery plugin is a new shortdoce by yours truly.

## TL;DR

```
{{< lightgallery >}}
```

Yup, this really is it.
Creates a gallery with all images in page bundle.

**Limitations** are:

- Can work with images from the page bundle, and from `/assets`; **not** from `/static`
- Plugins are not yet usable
- Only CDN downloads, no static JSS / CS files (you must be OK for your site using a CDN for this)
- Transitions don't seem to be working
- You can't configure absolutely most settings yet

**Bottom line** is that this is a very simple, opinionated gallery plugin for flexible but still simple use cases, which is hopefully expanded over time.

## Installation

**Either** (preferred variant) load the short code using Hugo's [modules](https://gohugo.io/hugo-modules/use-modules/):

```
# config.toml
[[module.imports]]
path = "github.com/flypenguin/hugo-shortcode-gallery"
```

... **or** just copy the `lightgallery.html` file into your site's `/layout/shortcodes` folder.

## Usage

Please go see the [showcase page](https://hugo-gallery-shortcode-demo.netlify.app/) (or its [GitHub repo](https://github.com/flypenguin/hugo-shortcode-gallery)) for documentation and exmaples.

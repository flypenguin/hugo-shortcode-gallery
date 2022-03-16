# Image galleries

The gallery plugin is a new shortdoce by yours truly.

## TL;DR

```
{{< lightgallery >}}
```

Yup, this really is it.
Creates a gallery with all images in page bundle.

**Limitations** are:

- You can't use images from `static/` directories at the moment, only (!) images from the page bundle.
- Plugins are not yet usable
- Only CDN downloads, no static JSS / CS files (you must be OK for your site using a CDN for this)
- Transitions don't seem to be working
- You can't configure absolutely most settings yet

**Bottom line** is that this is a very simple, opinionated gallery plugin for flexible but still simple use cases.

### Simple gallery with all images in the page bundle

```
{{< lightgallery >}}
```

Uses all images in the page bundle.

### Multiple galleries

```
{{< lightgallery glob="images/img1*.jpg" >}}
{{< lightgallery glob="images/img2*.jpg" id="gallery2>}}

OR

{{< lightgallery glob="images/img1*.jpg" id="gallery1" flags="load" >}}
{{< lightgallery glob="images/img2*.jpg" id="gallery2" >}}
```

CSS and javascript bundles are _only_ loaded when you do _not_ change the gallery id parameters (the default is "lightgallery").
If you change the id parameter on the first gallery you have to add the "load" flag.


### Select images by file name / glob expression

```
{{< lightgallery glob="images/**.jpg" >}}
```

Does what you think it does.
This is the way to have more than one gallery on a page.

### Image alts and captions

```
{{< lightgallery altslice=8 >}}
```
The caption is the image name (e.g. "IMG_1234" for the file "IMG_1234.jpg").
You can include a description in the image file name like this:

- `IMG_1234 this is my super cool image.jpg`

The suffix '.jpg' is removed automatically anyways.
`altslice=8` now always removes 8 characters from the front as well, so that alt image caption will be:

- "this is my super cool image"

### Thumbnails

```
{{< lightgallery thumbformat="webp" thumbsize="200x200" thumbquality="q75" thumbtype="fit" >}}
```

thumbformat, -size & quality are obvious.
thumbtype can be "fit" or "fill". "fit" will preserve aspect ratio, "fill" will sensibly crop all thumbnails to the dimensions in $thumbsize.

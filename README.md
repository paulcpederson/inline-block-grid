# Inline Block Grid

Simple grid system built with `display: inline-block`. For more about how this technique works, read the [blog post](http://paulcpederson.com/articles/inline-block-grid/).

## Install

Several ways to do this. Two are listed below:

### NPM Install It

```
npm install inline-block-grid --save-dev
```

If you do it this way, you can use with [node-sass](https://github.com/sass/node-sass#command-line-interface). Just use `--include-path node_modules/inline-block-grid/`.

### Drag and Drop It

1. Go to the [releases page](https://github.com/paulcpederson/inline-block-grid/releases).
2. Click the button to download a zip.
3. Decompress and drop in your SCSS folder.

### Plain CSS

The grid is also built to a plain css file, so if you aren't using sass or don't need any customization you can simply grab `grid.css` and add it to your project.

## Use

Whatever install method you used, now you can just:

```
@import 'inline-block-grid';
```

This will give you all the classes to start using the grid in your html.

## Examples

A simple two column layout would be as follows:

```
<div class="block-grid">
  <div class="column-6">
    ... some stuff
  </div>
  <div class="column-6">
    ... some other stuff
  </div>
</div>
```

Or a typical sidebar layout:

```
<div class="block-grid">
  <div class="column-2 post-1"></div>
  <div class="column-9"></div>
</div>
```

Or how about a product grid:

```
<div class="block-grid align-center">
  <div class="column-3"></div>
  <div class="column-3"></div>
  <div class="column-3"></div>
  <div class="column-3"></div>
  <div class="column-3"></div>
  <div class="column-3"></div>
  <div class="column-3"></div>
  <div class="column-3"></div>
  <div class="column-3"></div>
  <div class="column-3"></div>
  <div class="column-3"></div>
  <div class="column-3"></div>
</div>
```

## Class Reference

| class | description |
| ----- | ----------- |
| `.block-grid` | Wrap around columns (required) |
| `.column-X` | Amount of columns element should span (1-12) |
| `.pre-X` | Apply margin-left of `X` columns |
| `.post-X` | Apply margin-right of `X` columns |
| `.align-right` | Column group should right align orphan columns |
| `.align-center` | Column group should center orphan columns |
| `.align-baseline` | Column content aligned to baseline |

## Responsive Classes

For easy responsive layouts, each class is also available with `small-` and `medium-` prefixes. For example, to create an element that is full-width on a phone, half-width on a tablet, and quarter-width on a desktop:

```html
<div class="column-6 medium-column-12 small-column-24">
  <h1> Responsive Columns!</h1>
</div>
```

There are also responsive `pre` and `post` classes for spacing:

```html
<div class="column-4 pre-12 small-pre-6 medium-pre-2"></div>
```

### Responsive Class Reference

| class | description |
| ----- | ----------- |
| `small-column-X` | Width at small screen size |
| `small-pre-X` | Margin left at small screen size |
| `small-post-X` | Margin right at small screen size |
| `medium-column-X` | Width at medium screen size |
| `medium-pre-X` | Margin left at medium screen size |
| `medium-post-X` | Margin right at medium screen size |

## Customization

If you are using sass, you can customize several aspects of the grid:

| Variable | Description | Default |
| -------- | ----------- | ------- |
| `$column-count` | Number of columns in the grid | 12 |
| `$gutter` | Amount of space between the columns | 1rem |
| `$font-reset` | Default font family for your project | sans |
| `$size-small` | Small size breakpoint | 480px |
| `$size-medium` | Medium size breakpoint | 960px |

## License

>©Paul C Pederson 2015 under the [Fair License](http://en.wikipedia.org/wiki/Fair_License)

>Usage of the works is permitted provided that this instrument is retained with the works, so that any entity that uses the works is notified of this instrument.

>DISCLAIMER: THE WORKS ARE WITHOUT WARRANTY.

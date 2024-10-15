# Hinode Module - Lightbox for Boostrap 5

<!-- Tagline -->
<p align="center">
    <b>A Hugo module for [Lightbox for Boostrap 5](https://trvswgnr.github.io/bs5-lightbox/) that is compatible with Hinode</b>
    <br />
</p>

<!-- Badges -->
<p align="center">
    <a href="https://gohugo.io" alt="Hugo website">
        <img src="https://img.shields.io/badge/generator-hugo-brightgreen">
    </a>
    <a href="https://gethinode.com" alt="Hinode theme">
        <img src="https://img.shields.io/badge/theme-hinode-blue">
    </a>
</p>

## About

While I can't imagine anyone else wanting to use this, it loads the JS for the lightbox _after_ Bootstrap, which is required for the lightbox to work.

## Usage

The module is "optional" per default. In this case the module must be enabled in the frontmatter of the pages that use the lightbox by adding: `modules: ["bs5-lightbox"]`

To make it work with your images, you need to wrap a URL around it with the following params: `data-toggle="lightbox" data-gallery="gallery"`

Example:

```
<a href="{{ $image }}" data-toggle="lightbox" data-gallery="gallery">
    {{- partial "assets/image.html" (dict "url" {{ $image }} "ratio" "1x1" "wrapper" "mx-auto" "class" "img-fluid") -}}
</a>
```

### Shortcode

For the shortcode to content, your frontmatter must include:
```
----
modules: ["bs5-lightbox"]
photogallery:
 - /img/path/to/image1.jpg
 - /img/path/to/image2.jpg
----
```

And in your post content:

`{{< bs5-lightbox title="Alt text" >}}`

Images should be located in the `assets/img` folder, and will be resized by Hinode. If you don't use a title, it will use the page title.

## Contributing

This module uses [semantic-release][semantic-release] to automate the release of new versions. The package uses `husky` and `commitlint` to ensure commit messages adhere to the [Conventional Commits][conventionalcommits] specification. You can run `npx git-cz` from the terminal to help prepare the commit message.

<!-- ## Configuration

This module supports the following parameters (see the section `params.modules` in `config.toml`):

| Setting                   | Default | Description |
|---------------------------|---------|-------------| -->

<!-- MARKDOWN LINKS -->
[hugo]: https://gohugo.io
[hinode_docs]: https://gethinode.com
<!-- [module]: https://example.com -->
[repository]: https://github.com/gethinode/hinode.git
[repository_template]: https://github.com/gethinode/template.git
[conventionalcommits]: https://www.conventionalcommits.org
[husky]: https://typicode.github.io/husky/
[semantic-release]: https://semantic-release.gitbook.io/

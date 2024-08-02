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

While I can't imagine anyone else wanting to use this, it loads the JS for the lightbox _after_ Bootstrap.

## Usage

The module is "optional" per default. In this case the module must be enabled in the frontmatter of the pages that use mermaid by adding: `modules: ["bs5-lightbox"]`

To make it work with your images, you need to wrap a URL around it with the following params:

```
<a href="{{ $image }}" data-toggle="lightbox" data-gallery="gallery">
    {{- partial "assets/image.html" (dict "url" . "ratio" "1x1" "wrapper" "mx-auto" "class" "img-fluid") -}}
</a>
```

In my case, I did this in a a template, but you could convert it to a shortcode.

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

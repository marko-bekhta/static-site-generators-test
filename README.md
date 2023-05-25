# [Hexo](https://hexo.io/)

## How to try it locally

This is a JS based generator, so you'd need Node and npm to run things.
It is probably best to setup Node with [nvm](https://github.com/nvm-sh/nvm).
Once you have that in place - go to the project root and run:

```shell
# install any dependencies from package.json
npm install
```

After that you can either try the live preview (changes to the content files are automatically refreshed and become
visible):

```shell
hexo server
```

Or to only generate the resulting html/css/js files:

```shell
hexo generate
```

## Notes

* Supports multiple template engines, plugin that support HAML - is outdated and is not compatible with a current
  version.
* All these supported templates are "easier to read" since they are closer to HTML than what HAML looks like.
* Note: asciidoc is rendered via [Asciidoctor.js](https://docs.asciidoctor.org/asciidoctor.js/latest/)
* Didn't find a way to "inline" asciidoc -- so we'd need to write some own helper that'd use asciidoctor.js and do that
  ourselves ... Or change how we've structured some of the content.
* Code highlights for Asciidoctor.js will require some
  work. [Asciidoctor plugin](https://github.com/hcoona/hexo-renderer-asciidoc) doesn't have much docs and no obvious
  way to configure things.
* Data is added via YAML files and then can be referenced from the templates as if accessing a property of `site.data`
  with a name same
  as a filename.
* [scss plugin](https://github.com/mamboer/hexo-renderer-scss) failed to install so here a simple css is used (converted
  the scss from the main project).
* To download and process pom files we'd need to write a script and put it in the package json to run.
* Didn't see built in support for profiles (test/dev/stage/prod) so might need add that manually. I'm thinking about
  having a profile property set somewhere in config (can be passed as build parameter) that later will be used as a key
  to get properties...
* Docs mostly fine, simple overall, there's a lot of plugins but a lot of those are outdated.

# 11ty ([Eleventy](https://www.11ty.dev/docs/getting-started/))

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
npm run start
```

Or to only generate the resulting html/css/js files:

```shell
npm run build
```

## Notes

* Supports multiple template engines, even supports HAML (the template engine used by current sites) to some extent.
	Problem with using it is that the support is limited and the lib is outdated (https://github.com/creationix/haml-js)
* All these supported templates are "easier to read" since they are closer to HTML than what HAML looks like.
* Multiple template engines can be mixed. See how validator index (about) page is using njk while the rest is using ejs
	templates. (https://www.11ty.dev/docs/languages/)
* Rendering files to embed a md/asciidoc etc into a template is only supported by Nunjucks/Liquid/JavaScript (11ty.js)
	template engines. Besides including rendered files it can also render an inline template, but
	it looks like not all inline templates are rendered correctly. Have tried to render embedded asciidoc and it didn't
	work correctly. (https://www.11ty.dev/docs/plugins/render/)
* Note: asciidoc is rendered via [Asciidoctor.js](https://docs.asciidoctor.org/asciidoctor.js/latest/)
* Code highlights for Asciidoctor.js is using [Prism](https://prismjs.com/index.html) (
	tutorial https://saneef.com/tutorials/asciidoc-syntax-highlighting/)
* Data is added via JSON files and then can be referenced from the templates as if accessing a property with a name same
	as a filename (https://www.11ty.dev/docs/data-global/).
* Supports [using scss](https://www.11ty.dev/docs/languages/custom/#example-add-sass-support-to-eleventy) compared to
	Hexo (which had some plugin that didn't work). Note that for the scss to process the file -- it should be in the
	content folder, so if we'd want to do that -- just create a css sub folder under content and that's it.
* To download and process pom files we'd need to write a script and put it in the package json to run. Can also add it
	as a first command to existing build/run commands so that it get executed before the actual build happens.
* Didn't see built in support for profiles (test/dev/stage/prod) so might need add that manually. I'm thinking about
	having a profile property set somewhere in config (can be passed as build parameter) that later will be used as a key
	to get properties...
* OK docs, simple overall, intuitive structure, easy to add plugins.

# [Jekyll](https://jekyllrb.com/)

## How to try it locally

Before running need to [install](https://jekyllrb.com/docs/installation/):

```shell
sudo dnf install gcc-c++ ruby-devel
# in project folder:
gem install jekyll bundler
```

To start:

```shell
bundle exec jekyll serve
```

## Notes:

* Troubles installing Ruby -_-
* Liquid templates do not feel as intuitive as ejs/njk ones. But still better than HAML
* Asciidoc is rendered with an asciidoctor ruby gem (so all the troubles of installing gems but predictable results)
* Supports sass see this project example from docs https://github.com/jekyll/jekyll-sass-converter/tree/master/docs .
  Important to have a correct header in the file to get things processed.

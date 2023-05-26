# [Hugo](https://gohugo.io/)

## How to try it locally

First need to have Go
installed (https://go.dev/doc/install / https://developer.fedoraproject.org/tech/languages/go/go-installation.html ):

```shell
sudo dnf install golang
```
Then install hugo either with dnf or from snap:

```shell
sudo dnf install hugo
# or install hugo from snap instead of DNF:
sudo snap install hugo
```

To start a live preview:

```shell
hugo server
```

To generate the pages:

```shell
hugo
```

## Notes

* Docs looks nice.
* Has a similar functionality to profiles: https://gohugo.io/getting-started/configuration/#configuration-file
```shell
hugo --config debugconfig.toml
hugo --config a.toml,b.toml,c.toml
```
* Go templates are not as intuitive as the JS ones. (conditionals and other control structures in particular)
* To use asciidoc need to install it https://gohugo.io/content-management/formats/#list-of-content-formats. So we end up
  in a similar situation as in case of Jekyll with installing things... Didn't manage to make this work locally (while
  asciidoc commands execute OK from a terminal, they fail when are execute by Hugo) and didn't want to spend to much
  time to investigate further.
* This example doesn't have the project page ready as the hugo+theme kept "crashing"  
  * It not always render the index page in the preview (haven't figured out why)
  * Non-index static pages are not always rendered in live preview (haven't figured out why)

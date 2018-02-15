[![Docker Pulls](https://img.shields.io/docker/pulls/alperyilmaz/asciidoctor.svg)](https://hub.docker.com/r/alperyilmaz/asciidoctor/) [![Docker Automated buil](https://img.shields.io/docker/automated/alperyilmaz/asciidoctor.svg?style=flat-square)](https://hub.docker.com/r/alperyilmaz/asciidoctor/) [![Docker Build Statu](https://img.shields.io/docker/build/alperyilmaz/asciidoctor.svg?style=flat-square)](https://hub.docker.com/r/alperyilmaz/asciidoctor/) [![](https://images.microbadger.com/badges/image/alperyilmaz/asciidoctor.svg)](https://microbadger.com/images/alperyilmaz/asciidoctor "Get your own image badge on microbadger.com") [![](https://images.microbadger.com/badges/license/alperyilmaz/asciidoctor.svg)](https://microbadger.com/images/alperyilmaz/asciidoctor "Get your own license badge on microbadger.com")

# asciidoctor container

Asciidoctor container, based on `asciidoctor/docker-asciidoctor` container, includes more packages such as `asciidoctor-bibtex`, `asciidoctor-bibliography`, etc.

As of now, used mainly for revealjs presentations. The command below show how to render the presentations:

```bash
docker run --rm -v $(pwd):/documents alperyilmaz/asciidoctor asciidoctor-revealjs presentation-file.adoc
```

If the presentation file does not set some variables, they can be provided in the commandline:

```bash
docker run --rm -v $(pwd):/documents alperyilmaz/asciidoctor asciidoctor-revealjs -a revealjs_history=false -a revealjs_theme=white -a revealjs_slideNumber=true -a revealjsdir=reveal.js -a notitle presentation-file.adoc
```

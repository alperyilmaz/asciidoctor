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

A basic Red Hat style for the default Asciidoctor build.

# Local build 

```cmd
asciidoctor main.adoc -o index.html \
-a stylesheet="assets/css/redhat.css" \
-a toc \
-a toc-placement=left \
-a docinfodir=assets \
-a docinfo=shared \
-a source-highlighter=rouge \
-a rouge-style=github \
-a favicon=assets/img/favicon.ico \
-a icon-set=fab \
-a icons=font \
-a sectlinks
```

# Containerized build

Load the assets to the local context:
```cmd
$ podman cp $(podman run --quiet --detach quay.io/rhn_support_aireilly/asciidoctor-basic-style):/docs/assets ./assets
```

Run the build:
```cmd
$ podman run -v "$(pwd)":/docs:Z -v "$(pwd)/assets":/assets:Z quay.io/rhn_support_aireilly/asciidoctor-basic-style build main.adoc
```

CSS based on https://github.com/uroesch/asciidoctor-readthedocs-theme



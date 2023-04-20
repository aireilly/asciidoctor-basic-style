A basic AsciiDoctor style for the default Asciidoctor build. To build locally, run the following command: 

```cmd
asciidoctor -a stylesheet="assets/css/redhat.css" -a toc -a toc-placement=left \
-a icons=font -a docinfodir="assets" -a docinfo=shared \
-a source-highlighter=rouge -a rouge-style=github \
-a favicon="assets/images/favicon.ico" \
-a iconsdir="assets/images" -a icon-set=fab -a icons="font" \
-a sectlinks main.adoc -o index.html
```

CSS based on https://github.com/uroesch/asciidoctor-readthedocs-theme.
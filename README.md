A basic AsciiDoctor style for the default Asciidoctor build. To build locally, run the following command: 

```cmd
asciidoctor -a stylesheet="assets/css/redhat.css" -a toc -a toc-placement=left \
-a icons=font -a docinfodir="assets" -a docinfo=shared \
-a source-highlighter="highlight.js" -a favicon="assets/images/favicon.ico" \
-a iconsdir="assets/images" -a icon-set=fab -a icons="font" \
-a sectlinks main.adoc -o index.html
```
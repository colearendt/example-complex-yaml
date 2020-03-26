# Example Complex YAML

This R Markdown report has a complex YAML header that grabs options from a
static file.

A few caveats when deployed to RStudio Connect:

- You cannot use relative paths to reference resources deployed with RStudio
Connect
- Absolute system paths to available resources, as well as links to static URLs
/ etc. are welcome
- Related, environment variables (including secrets managed in RStudio Connect)
can be passed (see `TESTVAR`) from the parent process

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
- Package dependencies are not parsed in the YAML header, so you need to add the
package to a `library("packagename")` elsewhere in a R code chunk in order for
the dependency to be recognized

Aside from these caveats, you can use any code you want in that section! A few ideas for your exploration:

```r
# get a record from a table
!expr mycon <- DBI::dbConnect(odbc::odbc(), "My DSN"); DBI::dbGetQuery(mycon, "mytable")$mycolumn

# get a pin
!expr pins::board_register_rsconnect(name = "myrsc"); pin_get("sales-by-baths", board = "myrsc")$mycolumn
```

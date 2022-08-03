source("renv/activate.R")

# https://github.com/Rdatatable/data.table/issues/5425#issuecomment-1199209230
print_data_table <- function(x, ...) {
  # Adapted from data.table:::as.data.frame.data.table()
  ans <- x
  attr(ans, "row.names") <- .set_row_names(nrow(x))
  attr(ans, "class") <- c("tbl", "data.frame")
  attr(ans, "sorted") <- NULL
  attr(ans, ".internal.selfref") <- NULL
  print(ans)
  invisible(x)
}
assignInNamespace("print.data.table", print_data_table, asNamespace("data.table"))

options(datatable.prettyprint.char = 30L)

# Summary of changes #

  * Introduces a `current_error` member for each `Measurer`, which holds the error computed after each iteration. This only works with those measurers that compute a single real after each iteration.
  * `Linear.{h,cc}` was modified to allow all sorts for bias and weight decay options.
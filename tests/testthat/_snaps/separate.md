# too many pieces dealt with as requested

    Code
      separate(df, x, c("x", "y"))
    Warning <warning>
      Expected 2 pieces. Additional pieces discarded in 1 rows [2].
    Output
      # A tibble: 2 x 2
        x     y    
        <chr> <chr>
      1 a     b    
      2 a     b    

---

    Code
      separate(df, x, c("x", "y"), extra = "error")
    Warning <warning>
      `extra = "error"` is deprecated. Please use `extra = "warn"` instead
      Expected 2 pieces. Additional pieces discarded in 1 rows [2].
    Output
      # A tibble: 2 x 2
        x     y    
        <chr> <chr>
      1 a     b    
      2 a     b    

# too few pieces dealt with as requested

    Code
      separate(df, x, c("x", "y", "z"))
    Warning <warning>
      Expected 3 pieces. Missing pieces filled with `NA` in 1 rows [1].
    Output
      # A tibble: 2 x 3
        x     y     z    
        <chr> <chr> <chr>
      1 a     b     <NA> 
      2 a     b     c    

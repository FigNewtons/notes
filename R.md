R Command Sheet 
===============================================================================

Basic R Commands
-------------------------------------------------------------------------------

+----------------------------------+------------------------------------------+
|Name                              | Description                              |
+==================================+==========================================+
|aggregate(x, ...)                 | Splits data into subsets and computes    |
|                                  | summary stats for each (or applies a     |
|                                  | specified function)                      |
+----------------------------------+------------------------------------------+
|args(name)                        | Returns the function header of _name_,   | 
|                                  | displaying the arguments it takes        |
+----------------------------------+------------------------------------------+
|attributes(obj) <- values         | Gets or sets an object's attributes      |
+----------------------------------+------------------------------------------+
|c()                               | Concatentation (creates a vector)	      |
+----------------------------------+------------------------------------------+
|cbind() / rbind()                 | Add column/row to a matrix or dataframe  |
+----------------------------------+------------------------------------------+
|character(length = 0)             | Creates a character vector of a given    |
|                                  | length; includes _is_ and _as_ methods   |
|                                  | for logical testing and conversion,      |
|                                  | respectively                             |
+----------------------------------+------------------------------------------+
|class() / unclass()               | Tells you the class of an object/        |
|                                  | Shows you the internal rep. of an object | 
+----------------------------------+------------------------------------------+
|* colMeans(x) / rowMeans(x)       | * Return the mean of each row/column in  |
|                                  | numeric array _x_                        |
|* colnames(x) / rownames(x)       | * Get or set a column/row for a matrix or|
|                                  | dataframe                                |
|* colSums(x) / rowSums(x)         | * Return the sum of each row/column in   |
|                                  | numeric array _x_                        |
+----------------------------------+------------------------------------------+
|complete.cases()                  | Returns a logical vector based on rows   |
|                                  | without missing values (NAs)             |
+----------------------------------+------------------------------------------+
|data()                            | Loads a data into the workspace          |
+----------------------------------+------------------------------------------+
|data.frame()                      | Creates a data frame                     |
+----------------------------------+------------------------------------------+
|date()                            | Returns current system date              |
+----------------------------------+------------------------------------------+
|dim(x) <- value                   | Gets or sets the dimension of an object  |
+----------------------------------+------------------------------------------+
|dir()                             | List files in the working directory      |
+----------------------------------+------------------------------------------+
|dir.create()                      | Creates a folder in the working directory|
|                                  | (Has recursive mode for subdirectories,  |
|                                  | which is off by default)                 |
+----------------------------------+------------------------------------------+
|environment(fun = NULL)           | Prints the environment of function _fun_ |
+----------------------------------+------------------------------------------+
|factor(x, levels, labels, ordered)| Creates a factor object                  |
+----------------------------------+------------------------------------------+
|get(x)                            | Fetches object(s) by name                | 
+----------------------------------+------------------------------------------+
|getwd(dir)                        | Sets the working directory to _dir_      | 
+----------------------------------+------------------------------------------+
|head(x, n = 6L) / tail(x, n = 6L) | Displays the first/last _n_ lines of an  | 
|                                  | object                                   |
+----------------------------------+------------------------------------------+
|install.packages(pkgs)            | Install the list of _pkgs_ from CRAN     |
+----------------------------------+------------------------------------------+
|invisible(x)                      | Prevents the automatic printing of an    |
|                                  | object                                   |
+----------------------------------+------------------------------------------+
|length(x)                         |Returns the length of an object           |
+----------------------------------+------------------------------------------+
|library(package)                  | Loads an R package environment for use;  |
|                                  | _package_ is without quotes, and         |
|                                  | _help = package_ gives us documentation  |
+----------------------------------+------------------------------------------+
|ls()                              | List the objects in R's local workspace  |
+----------------------------------+------------------------------------------+
|matrix(data=NA,nrow = 1,ncol = 1) | Creates a matrix from _data_             |
+----------------------------------+------------------------------------------+
|names(x) <- value                 |Get or set the names of an object         |
+----------------------------------+------------------------------------------+
|nrow(x) / ncol(x)                 | Returns the no. of rows/columns in _x_   |
+----------------------------------+------------------------------------------+
|paste(..., collapse=NULL)         | Join vectors into a string;the _collapse_|
|                                  | argument tells us what to put in between |
|                                  | each vector upon concatenation;the _sep_ |
|                                  | argument tells us what to put in betwen  |
|                                  | elements within a vector                 |
+----------------------------------+------------------------------------------+
|print(x)						   | Prints _x_                               |
+----------------------------------+------------------------------------------+
|rep(x, times= 1, each = 1)        | Repeats _x_ by a specified no. of times; |
|                                  | the _each_ parameter allows us to repeat |
|                                  | element-wise in a vector                 |
+----------------------------------+------------------------------------------+
|seq(from, to, by)                 | Generates regular sequences              |
+----------------------------------+------------------------------------------+
|seq_along(x)                      | Generates sequence from 1, ..., length(x)|
+----------------------------------+------------------------------------------+
|setwd(dir)                        | Changes the working directory to _dir_   |
+----------------------------------+------------------------------------------+
|stop()                            | Stops execution and throws an error with |
|                                  | a provided message                       |
+----------------------------------+------------------------------------------+
|str(x)                            | Displays the structure of x              |
+----------------------------------+------------------------------------------+
|summary(x)                        | Displays the summary stats for x         |
+----------------------------------+------------------------------------------+
|tables()                          | List all tables in the workspace         |
+----------------------------------+------------------------------------------+
|unique(x)                         |Returns the unique values of an object x  |
+----------------------------------+------------------------------------------+
|unlink(x)                         | Deletes a file or directory; recursive   |
|                                  | and force deletion are false by default  |
+----------------------------------+------------------------------------------+
|vector(mode="logical", length = 0)| Creates a vector of a certain mode and   |
|                                  | length                                   |
+----------------------------------+------------------------------------------+

Debugging Functions
-------------------------------------------------------------------------------

+----------------------------------+------------------------------------------+
|Name                              | Description                              |
+==================================+==========================================+
|browser()                         | Suspends execution of a function and puts|
|                                  | in debug mode                            |
+----------------------------------+------------------------------------------+
|debug()                           | Flags a function to "step in" line by    |
|                                  | line in debug mode                       |
+----------------------------------+------------------------------------------+
|recover()                         | Modifies error behavior so you can look  |
|                                  | at function stack                        |
+----------------------------------+------------------------------------------+
|Rprof()                           | Starts R profiler                        |
+----------------------------------+------------------------------------------+
|summaryRprof()                    | Summarizes output from R profiler        |
+----------------------------------+------------------------------------------+
|trace()                           | Allows user to insert debugging code into|
|                                  | a function                               |
+----------------------------------+------------------------------------------+
|traceback()                       | Prints function stack to last call when  |
|                                  | error occurred                           |
+----------------------------------+------------------------------------------+






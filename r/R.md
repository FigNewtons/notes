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
|file.path(...)                    | Construct file path from components      |
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
|nchar(x)                          | Returns length of string/character vector|
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
|range()                           | Returns a vector with the min and max    |
+----------------------------------+------------------------------------------+
|rep(x, times= 1, each = 1)        | Repeats _x_ by a specified no. of times; |
|                                  | the _each_ parameter allows us to repeat |
|                                  | element-wise in a vector                 |
+----------------------------------+------------------------------------------+
|require(package)                  | Similar to library(), but returns a truth|
|                                  | value if package is found                |
+----------------------------------+------------------------------------------+
|rm(..., list = character())       | Removes objects from an environment      |
+----------------------------------+------------------------------------------+
|seq(from, to, by)                 | Generates regular sequences              |
+----------------------------------+------------------------------------------+
|seq_along(x)                      | Generates sequence from 1, ..., length(x)|
+----------------------------------+------------------------------------------+
|setwd(dir)                        | Changes the working directory to _dir_   |
+----------------------------------+------------------------------------------+
|source(file)                      | Read R code from a file or connection    |
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

Files and Reading Data
-------------------------------------------------------------------------------

The basic ways to read in data come from the read.* functions:

* read.table()
* read.csv()
* read.delim()

Working with Text
-------------------------------------------------------------------------------

For pattern matching, we have the almighty _grep_ function.

* grep(pattern, x, ignore.case = FALSE, perl = FALSE, value = FALSE, 
        fixed = FALSE, useBytes = FALSE, invert = FALSE)
        
By default, grep returns the indices of matches. If you want a logical vector
instead, use _grepl_. For pattern substitutions, use _sub_ and _gsub_ : the
former replaces just the first occurrence while the latter replaces all
occurrences. In both cases, we have an added _replacement_ argument:

* sub(pattern, replacement, x)
        
Arguments:
* _pattern_ is your regex pattern
* _x_ is the vector you want match the pattern against
* _ignore.case_ turns off case-sensitive matching
* _perl_ allows Perl-style regexes
* _value_ returns a vector of the matched strings
* _fixed_ forces _pattern_ to be matched as-is
* _useBytes_ matching done by byte rather than by character
* _invert_ returns the strings that don't match


Probability and Sampling
-------------------------------------------------------------------------------

Probability distributions have four forms:

* r--- - Randomly sample the distribution
* d--- - Density function
* p--- - Distribution function
* q--- - Quantile function 

Some of the distributions available (preface it with an above letter):

* beta - Beta
* binom - Binomial 
* cauchy - Cauchy
* exp - Exponential
* gamma - Gamma
* geom - Geometric
* norm - Normal (Gaussian)
* pois - Poisson 
* unif - Uniform
* weibull - Weibull


Time
-------------------------------------------------------------------------------
There are two classes in R used to represent time: 

* POSIXct : Unix time (time represented as seconds from January 1, 1970)
* POSIXlt : Time represented as named list (sec, min, mday, mon, year, etc)

[List of time formatters](http://unixhelp.ed.ac.uk/CGI/man-cgi?date)

+----------------------------------+------------------------------------------+
|Name                              | Description                              |
+==================================+==========================================+
|date()                            | Returns current date                     |
+----------------------------------+------------------------------------------+
|difftime(t2, t1, tz,			   | Returns the time difference (t2 - t1)    |
|   units = c("auto","secs",       |                                          |
|   "mins","hours","days","weeks"))|                                          |
+----------------------------------+------------------------------------------+
|strptime(x, format, tz="")        | Converts x into a suitable time object   |
+----------------------------------+------------------------------------------+
|Sys.time(x)                       | Returns the current system time          |
+----------------------------------+------------------------------------------+


### Lubridate

[Here is the lubridate documentation]
(cran.r-project.org/web/packages/lubridate/lubridate.pdf)

Timespans are either duration, interval, or period objects. 

+----------------------------------+------------------------------------------+
|Name                              | Description                              |
+==================================+==========================================+
|am(x) / pm(x)                     | Returns TRUE if _x_ occurs in the AM / PM|
+----------------------------------+------------------------------------------+
|hms(x) / ms(x) / ymd(x), etc      | Returns a period object based on the     |
|                                  | order and letters of the function        |
|                                  | (y = year, m = month, d = day, h = hour, |
|                                  | s = second)                              |
+----------------------------------+------------------------------------------+
|leap_year(x)                      | Returns TRUE if _x_ is a leap year       |
+----------------------------------+------------------------------------------+
|now(x) / today(x)                 | Returns the current time; today returns  |
|                                  | YYYY-MM-DD while now includes HH:MM:SS TZ|
+----------------------------------+------------------------------------------+
|a %within% b                      | Returns TRUE if time _a_ is within       | 
|                                  | interval _b_                             |
+----------------------------------+------------------------------------------+
| * hour(x)                        | Gets /sets the time unit specified; _tz_ |
| * minute(x)                      | stands for "time zone"; _quarter_        |
| * month(x)                       | returns Q1-Q4                            |
| * quarter(x)                     |                                          |
| * second(x)                      |                                          |
| * tz(x)                          |                                          |
| * weekday(x)                     |                                          |
| * year(x)                        |                                          |
+----------------------------------+------------------------------------------+
|weekdays(x)                       | Returns the name of the day of the week  |
+----------------------------------+------------------------------------------+

Graphics
-------------------------------------------------------------------------------

The following are functions in the base package:

+----------------------------------+------------------------------------------+
|Name                              | Description                              |
+==================================+==========================================+
|boxplot(x)                        | Generates a box-and-whisker plot         |
+----------------------------------+------------------------------------------+
|hist(x)                           | Generates a histogram of x               |
+----------------------------------+------------------------------------------+
|plot(x)                           | Generates a scatterplot                  |
+----------------------------------+------------------------------------------+

### ggplot2


Swirl
-------------------------------------------------------------------------------

[The official page](http://swirlstats.com/)

These are the basic commands within swirl:

+----------------------------------+------------------------------------------+
|Name                              | Description                              |
+==================================+==========================================+
|bye()                             | Saves progress and exits                 |
+----------------------------------+------------------------------------------+
|info()                            | Display list of commands and their uses  |
+----------------------------------+------------------------------------------+
|nxt()                             | Continue the swirl lesson                |
+----------------------------------+------------------------------------------+
|play()                            | Pauses swirl to go into "sandbox" mode   |
+----------------------------------+------------------------------------------+
|skip()                            | Skips current lesson question            |
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






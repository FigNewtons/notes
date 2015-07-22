R Command Sheet
===============

Basic R Commands
----------------

<table>
<col width="44%" />
<col width="55%" />
<thead>
<tr class="header">
<th align="left">Name</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>aggregate(x, ...)</p></td>
<td align="left"><p>Splits data into subsets and computes summary stats for each (or applies a specified function)</p></td>
</tr>
<tr class="even">
<td align="left"><p>args(name)</p></td>
<td align="left"><p>Returns the function header of <em>name</em>, displaying the arguments it takes</p></td>
</tr>
<tr class="odd">
<td align="left"><p>attributes(obj) &lt;- values</p></td>
<td align="left"><p>Gets or sets an object's attributes</p></td>
</tr>
<tr class="even">
<td align="left"><p>c()</p></td>
<td align="left"><p>Concatentation (creates a vector)</p></td>
</tr>
<tr class="odd">
<td align="left"><p>cbind() / rbind()</p></td>
<td align="left"><p>Add column/row to a matrix or dataframe</p></td>
</tr>
<tr class="even">
<td align="left"><p>character(length = 0)</p></td>
<td align="left"><p>Creates a character vector of a given length; includes <em>is</em> and <em>as</em> methods for logical testing and conversion, respectively</p></td>
</tr>
<tr class="odd">
<td align="left"><p>class() / unclass()</p></td>
<td align="left"><p>Tells you the class of an object/ Shows you the internal rep. of an object</p></td>
</tr>
<tr class="even">
<td align="left"><ul>
<li><p>colMeans(x) / rowMeans(x)</p></li>
<li><p>colnames(x) / rownames(x)</p></li>
<li><p>colSums(x) / rowSums(x)</p></li>
</ul></td>
<td align="left"><ul>
<li>Return the mean of each row/column in numeric array <em>x</em></li>
<li>Get or set a column/row for a matrix or dataframe</li>
<li>Return the sum of each row/column in numeric array <em>x</em></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>complete.cases()</p></td>
<td align="left"><p>Returns a logical vector based on rows without missing values (NAs)</p></td>
</tr>
<tr class="even">
<td align="left"><p>cut(x)</p></td>
<td align="left"><p>Divides the range of x into intervals to be broken into factors</p></td>
</tr>
<tr class="odd">
<td align="left"><p>data()</p></td>
<td align="left"><p>Loads a data into the workspace</p></td>
</tr>
<tr class="even">
<td align="left"><p>data.frame()</p></td>
<td align="left"><p>Creates a data frame</p></td>
</tr>
<tr class="odd">
<td align="left"><p>dim(x) &lt;- value</p></td>
<td align="left"><p>Gets or sets the dimension of an object</p></td>
</tr>
<tr class="even">
<td align="left"><p>dir()</p></td>
<td align="left"><p>List files in the working directory</p></td>
</tr>
<tr class="odd">
<td align="left"><p>dir.create()</p></td>
<td align="left"><p>Creates a folder in the working directory (Has recursive mode for subdirectories, which is off by default)</p></td>
</tr>
<tr class="even">
<td align="left"><p>environment(fun = NULL)</p></td>
<td align="left"><p>Prints the environment of function <em>fun</em></p></td>
</tr>
<tr class="odd">
<td align="left"><p>factor(x, levels, labels, ordered)</p></td>
<td align="left"><p>Creates a factor object</p></td>
</tr>
<tr class="even">
<td align="left"><p>file.path(...)</p></td>
<td align="left"><p>Construct file path from components</p></td>
</tr>
<tr class="odd">
<td align="left"><p>get(x)</p></td>
<td align="left"><p>Fetches object(s) by name</p></td>
</tr>
<tr class="even">
<td align="left"><p>getwd(dir)</p></td>
<td align="left"><p>Sets the working directory to <em>dir</em></p></td>
</tr>
<tr class="odd">
<td align="left"><p>head(x, n = 6L) / tail(x, n = 6L)</p></td>
<td align="left"><p>Displays the first/last <em>n</em> lines of an object</p></td>
</tr>
<tr class="even">
<td align="left"><p>install.packages(pkgs)</p></td>
<td align="left"><p>Install the list of <em>pkgs</em> from CRAN</p></td>
</tr>
<tr class="odd">
<td align="left"><p>invisible(x)</p></td>
<td align="left"><p>Prevents the automatic printing of an object</p></td>
</tr>
<tr class="even">
<td align="left"><p>length(x)</p></td>
<td align="left"><p>Returns the length of an object</p></td>
</tr>
<tr class="odd">
<td align="left"><p>library(package)</p></td>
<td align="left"><p>Loads an R package environment for use; <em>package</em> is without quotes, and <em>help = package</em> gives us documentation</p></td>
</tr>
<tr class="even">
<td align="left"><p>ls()</p></td>
<td align="left"><p>List the objects in R's local workspace</p></td>
</tr>
<tr class="odd">
<td align="left"><p>matrix(data=NA,nrow = 1,ncol = 1)</p></td>
<td align="left"><p>Creates a matrix from <em>data</em></p></td>
</tr>
<tr class="even">
<td align="left"><p>names(x) &lt;- value</p></td>
<td align="left"><p>Get or set the names of an object</p></td>
</tr>
<tr class="odd">
<td align="left"><p>nchar(x)</p></td>
<td align="left"><p>Returns length of string/character vector</p></td>
</tr>
<tr class="even">
<td align="left"><p>nrow(x) / ncol(x)</p></td>
<td align="left"><p>Returns the no. of rows/columns in <em>x</em></p></td>
</tr>
<tr class="odd">
<td align="left"><p>outer(X, Y, FUN)</p></td>
<td align="left"><p>Computes the outer product of two arrays</p></td>
</tr>
<tr class="even">
<td align="left"><p>paste(..., collapse=NULL)</p></td>
<td align="left"><p>Join vectors into a string;the <em>collapse</em> argument tells us what to put in between each vector upon concatenation;the <em>sep</em> argument tells us what to put in betwen elements within a vector</p></td>
</tr>
<tr class="odd">
<td align="left"><p>print(x)</p></td>
<td align="left"><p>Prints <em>x</em></p></td>
</tr>
<tr class="even">
<td align="left"><p>range()</p></td>
<td align="left"><p>Returns a vector with the min and max</p></td>
</tr>
<tr class="odd">
<td align="left"><p>rep(x, times= 1, each = 1)</p></td>
<td align="left"><p>Repeats <em>x</em> by a specified no. of times; the <em>each</em> parameter allows us to repeat element-wise in a vector</p></td>
</tr>
<tr class="even">
<td align="left"><p>require(package)</p></td>
<td align="left"><p>Similar to library(), but returns a truth value if package is found</p></td>
</tr>
<tr class="odd">
<td align="left"><p>rm(..., list = character())</p></td>
<td align="left"><p>Removes objects from an environment</p></td>
</tr>
<tr class="even">
<td align="left"><p>savehistory() / loadhistory()</p></td>
<td align="left"><p>Saves or loads session command history</p></td>
</tr>
<tr class="odd">
<td align="left"><p>scale(x, center=TRUE, scale=TRUE)</p></td>
<td align="left"><p>Centers and/or scales the columns of a numeric matrix</p></td>
</tr>
<tr class="even">
<td align="left"><p>seq(from, to, by)</p></td>
<td align="left"><p>Generates regular sequences</p></td>
</tr>
<tr class="odd">
<td align="left"><p>seq_along(x)</p></td>
<td align="left"><p>Generates sequence from 1, ..., length(x)</p></td>
</tr>
<tr class="even">
<td align="left"><p>setwd(dir)</p></td>
<td align="left"><p>Changes the working directory to <em>dir</em></p></td>
</tr>
<tr class="odd">
<td align="left"><p>source(file)</p></td>
<td align="left"><p>Read R code from a file or connection</p></td>
</tr>
<tr class="even">
<td align="left"><p>stop()</p></td>
<td align="left"><p>Stops execution and throws an error with a provided message</p></td>
</tr>
<tr class="odd">
<td align="left"><p>str(x)</p></td>
<td align="left"><p>Displays the structure of x</p></td>
</tr>
<tr class="even">
<td align="left"><p>summary(x)</p></td>
<td align="left"><p>Displays the summary stats for x</p></td>
</tr>
<tr class="odd">
<td align="left"><p>t(x)</p></td>
<td align="left"><p>Transposes a matrix or data frame</p></td>
</tr>
<tr class="even">
<td align="left"><p>tables()</p></td>
<td align="left"><p>List all tables in the workspace</p></td>
</tr>
<tr class="odd">
<td align="left"><p>unique(x)</p></td>
<td align="left"><p>Returns the unique values of an object x</p></td>
</tr>
<tr class="even">
<td align="left"><p>unlink(x)</p></td>
<td align="left"><p>Deletes a file or directory; recursive and force deletion are false by default</p></td>
</tr>
<tr class="odd">
<td align="left"><p>vector(mode=&quot;logical&quot;, length = 0)</p></td>
<td align="left"><p>Creates a vector of a certain mode and length</p></td>
</tr>
<tr class="even">
<td align="left"><p>View(x, title)</p></td>
<td align="left"><p>Displays a spreadsheet-like data viewer</p></td>
</tr>
</tbody>
</table>

Files and Reading Data
----------------------

The basic ways to read in data come from the read.\* functions:

-   read.table()
-   read.csv()
-   read.delim()

Working with Text
-----------------

For pattern matching, we have the almighty *grep* function.

-   grep(pattern, x, ignore.case = FALSE, perl = FALSE, value = FALSE,
    fixed = FALSE, useBytes = FALSE, invert = FALSE)

By default, grep returns the indices of matches. If you want a logical
vector instead, use *grepl*. For pattern substitutions, use *sub* and
*gsub* : the former replaces just the first occurrence while the latter
replaces all occurrences. In both cases, we have an added *replacement*
argument:

-   sub(pattern, replacement, x)

Arguments:

-   *pattern* is your regex pattern
-   *x* is the vector you want match the pattern against
-   *ignore.case* turns off case-sensitive matching
-   *perl* allows Perl-style regexes
-   *value* returns a vector of the matched strings
-   *fixed* forces *pattern* to be matched as-is
-   *useBytes* matching done by byte rather than by character
-   *invert* returns the strings that don't match

Probability and Sampling
------------------------

Probability distributions have four forms:

-   r--- - Randomly sample the distribution
-   d--- - Density function
-   p--- - Distribution function
-   q--- - Quantile function

Some of the distributions available (preface it with an above letter):

-   beta - Beta
-   binom - Binomial
-   cauchy - Cauchy
-   exp - Exponential
-   gamma - Gamma
-   geom - Geometric
-   norm - Normal (Gaussian)
-   pois - Poisson
-   unif - Uniform
-   weibull - Weibull

dplyr / tidyr
-------------

The R packages dplyr and tidyr were created by Hadley Wickham as a way
to simplify and streamline the data analysis pipeline; dplyr is used for
data manipulation while tidyr is used for cleaning untidy datasets.

With dplyr, we have a few verbs that encompass most of our data
manipulation tasks. But first, it's perferable to use tbl\_df() and
tbl\_dt() for data frames and data tables, respectively, for a nicer way
to represent the dataset you want to work with:

<table>
<col width="44%" />
<col width="55%" />
<thead>
<tr class="header">
<th align="left">Name</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>filter()</p></td>
<td align="left"><p>Returns a subset of rows in a data frame</p></td>
</tr>
<tr class="even">
<td align="left"><p>slice()</p></td>
<td align="left"><p>Select rows by position</p></td>
</tr>
<tr class="odd">
<td align="left"><p>arrange()</p></td>
<td align="left"><p>Orders by columns; use desc() for descending order</p></td>
</tr>
<tr class="even">
<td align="left"><p>select()</p></td>
<td align="left"><p>Select columns; the : operator allows inclusive selection by column name; the - operator excludes columns</p></td>
</tr>
<tr class="odd">
<td align="left"><p>rename()</p></td>
<td align="left"><p>Similar to select except you can rename column names at the same time</p></td>
</tr>
<tr class="even">
<td align="left"><p>distinct()</p></td>
<td align="left"><p>Return unique values in table; generally used with select (like in SQL)</p></td>
</tr>
<tr class="odd">
<td align="left"><p>mutate()</p></td>
<td align="left"><p>Adds columns to table; more flexible than transform()</p></td>
</tr>
<tr class="even">
<td align="left"><p>transmutate()</p></td>
<td align="left"><p>Keeps just the variables you created</p></td>
</tr>
<tr class="odd">
<td align="left"><p>summarize()</p></td>
<td align="left"><p>Condenses multiple values into a single value</p></td>
</tr>
<tr class="even">
<td align="left"><p>inner_join(x, y, by = NULL)</p></td>
<td align="left"><p>Joins two tables together; there's also left, right, full joins, etc. just like in SQL</p></td>
</tr>
</tbody>
</table>

It is important to realize that we can chain many of these operations
together if we are dealing with a single dataset by using the %\>%
operator.

Now for the tidyr functions:

<table>
<col width="44%" />
<col width="55%" />
<thead>
<tr class="header">
<th align="left">Name</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>gather(data, key, value, ...)</p></td>
<td align="left"><p>Collapses multiple columns into key-value pairs</p></td>
</tr>
<tr class="even">
<td align="left"><p>separate(data, col, into, sep)</p></td>
<td align="left"><p>Separate one column into multiple columns</p></td>
</tr>
<tr class="odd">
<td align="left"><p>unite(data, col, ..., sep = &quot;_&quot;)</p></td>
<td align="left"><p>Unite mutliple columns into one</p></td>
</tr>
<tr class="even">
<td align="left"><p>spread(data, key, value)</p></td>
<td align="left"><p>Spread a key-value pair across multiple columns</p></td>
</tr>
</tbody>
</table>

Time
----

There are two classes in R used to represent time:

-   POSIXct : Unix time (time represented as seconds from January 1,
    1970)
-   POSIXlt : Time represented as named list (sec, min, mday, mon, year,
    etc)

[List of time formatters](http://unixhelp.ed.ac.uk/CGI/man-cgi?date)

<table>
<col width="44%" />
<col width="55%" />
<thead>
<tr class="header">
<th align="left">Name</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>date()</p></td>
<td align="left"><p>Returns current date</p></td>
</tr>
<tr class="even">
<td align="left"><p>difftime(t2, t1, tz, units = c(&quot;auto&quot;,&quot;secs&quot;, &quot;mins&quot;,&quot;hours&quot;,&quot;days&quot;,&quot;weeks&quot;))</p></td>
<td align="left"><p>Returns the time difference (t2 - t1)</p></td>
</tr>
<tr class="odd">
<td align="left"><p>strptime(x, format, tz=&quot;&quot;)</p></td>
<td align="left"><p>Converts x into a suitable time object</p></td>
</tr>
<tr class="even">
<td align="left"><p>Sys.time(x)</p></td>
<td align="left"><p>Returns the current system time</p></td>
</tr>
</tbody>
</table>

### Lubridate

[Here is the lubridate documentation]
(cran.r-project.org/web/packages/lubridate/lubridate.pdf)

Timespans are either duration, interval, or period objects.

<table>
<col width="44%" />
<col width="55%" />
<thead>
<tr class="header">
<th align="left">Name</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>am(x) / pm(x)</p></td>
<td align="left"><p>Returns TRUE if <em>x</em> occurs in the AM / PM</p></td>
</tr>
<tr class="even">
<td align="left"><p>hms(x) / ms(x) / ymd(x), etc</p></td>
<td align="left"><p>Returns a period object based on the order and letters of the function (y = year, m = month, d = day, h = hour, s = second)</p></td>
</tr>
<tr class="odd">
<td align="left"><p>leap_year(x)</p></td>
<td align="left"><p>Returns TRUE if <em>x</em> is a leap year</p></td>
</tr>
<tr class="even">
<td align="left"><p>now(x) / today(x)</p></td>
<td align="left"><p>Returns the current time; today returns YYYY-MM-DD while now includes HH:MM:SS TZ</p></td>
</tr>
<tr class="odd">
<td align="left"><p>a %within% b</p></td>
<td align="left"><p>Returns TRUE if time <em>a</em> is within interval <em>b</em></p></td>
</tr>
<tr class="even">
<td align="left"><ul>
<li>hour(x)</li>
<li>minute(x)</li>
<li>month(x)</li>
<li>quarter(x)</li>
<li>second(x)</li>
<li>tz(x)</li>
<li>weekday(x)</li>
<li>year(x)</li>
</ul></td>
<td align="left">Gets /sets the time unit specified; <em>tz</em> stands for &quot;time zone&quot;; <em>quarter</em> returns Q1-Q4</td>
</tr>
<tr class="odd">
<td align="left"><p>weekdays(x)</p></td>
<td align="left"><p>Returns the name of the day of the week</p></td>
</tr>
</tbody>
</table>

Graphics
--------

The following are functions in the base package:

<table>
<col width="44%" />
<col width="55%" />
<thead>
<tr class="header">
<th align="left">Name</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>abline(a = NULL, b = NULL)</p></td>
<td align="left"><p>Adds a straight line through current plot Arguments: a = intercept, b = slope</p></td>
</tr>
<tr class="even">
<td align="left"><p>boxplot(x)</p></td>
<td align="left"><p>Generates a box-and-whisker plot</p></td>
</tr>
<tr class="odd">
<td align="left"><p>contour(x, y, z)</p></td>
<td align="left"><p>Generates a contour plot z = f(x,y)</p></td>
</tr>
<tr class="even">
<td align="left"><p>hist(x)</p></td>
<td align="left"><p>Generates a histogram of x</p></td>
</tr>
<tr class="odd">
<td align="left"><p>plot(x)</p></td>
<td align="left"><p>Generates a scatterplot</p></td>
</tr>
<tr class="even">
<td align="left"><p>pairs(x)</p></td>
<td align="left"><p>Generates a matrix of scatterplots along every two variables in the dataset</p></td>
</tr>
</tbody>
</table>

Use *dev* to control your graphics devices. For example, dev.off() turns
off the current device (this is very helpful when plotting and using
different graphics libraries in one session)

### ggplot2

There are two basic ways to create a plot with ggplot2: qplot and
ggplot. For quick plots, use the former (it is similar to plot()). On
the other hand, ggplot is based on what's called the Grammar of
Graphics, and so ggplot has different syntax. Briefly, you'll have
ggplot plus a series of layers. Layers include:

-   Data
-   Aesthetic mappings (aes)
-   Geometric objects (geom)
-   Statistical transformations (stat)
-   Position adjustment (position)

Most likely, you'll end up with code that looks like this (form-wise):
\> ggplot(data, aes(x, y)) + geom\_point() + ...

Because of this layered approach, it becomes simple to create more
complicated graphics. If you want to save your plot, use ggsave.

Perhaps you want to break up your data by factor; that is, you want to
create a plot for each category of a factor. We can do this by faceting:
ggplot partitions a plot into a matrix of panels.

We'll now show some examples:

> library(ggplot2)

> qplot(carat, price, data = diamonds) \# Simple scatterplot
> ggplot(diamonds, aes(carat, price)) + geom\_point() \# Same plot as
> above

> qplot(hwy, cty, data = mpg, geom = "jitter") ggplot(mpg, aes(hwy,
> cty)) + geom\_jitter()

> qplot(reorder(class, hwy), hwy, data = mpg, geom = c("jitter",
> "boxplot")) ggplot(mpg, aes(reorder(class, hwy), hwy)) +
> geom\_jitter() + geom\_boxplot()

> qplot(log10(carat), log10(price), data = diamonds, color = color) +
> geom\_smooth(method = "lm") ggplot(diamonds, aes(log10(carat),
> log10(price), color = color)) + geom\_point() + geom\_smooth(method =
> "lm")

<table>
<col width="44%" />
<col width="55%" />
<thead>
<tr class="header">
<th align="left">Name</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>qplot()</p></td>
<td align="left"><p>Creates a quick plot</p></td>
</tr>
<tr class="even">
<td align="left"><p>ggplot()</p></td>
<td align="left"><p>Initializes a ggplot object</p></td>
</tr>
<tr class="odd">
<td align="left"><p>ggsave()</p></td>
<td align="left"><p>Saves a plot</p></td>
</tr>
<tr class="even">
<td align="left"><p>last_plot()</p></td>
<td align="left"><p>Retrieves the last plot called</p></td>
</tr>
<tr class="odd">
<td align="left"><p>resolution()</p></td>
<td align="left"><p>Returns the smallest non-zero distance between adjacent values</p></td>
</tr>
<tr class="even">
<td align="left"><p>xlim() / ylim()</p></td>
<td align="left"><p>Set the limits for the x and y axis, resp</p></td>
</tr>
<tr class="odd">
<td align="left"><p>facet_wrap(~cell)</p></td>
<td align="left"><p>Creates a 1D strip of panels based on a single factor, wrapping it into 2D</p></td>
</tr>
<tr class="even">
<td align="left"><p>facet_grid(row ~ col)</p></td>
<td align="left"><p>Creates a 2D matrix of panels based on two factors</p></td>
</tr>
</tbody>
</table>

Swirl
-----

[The official page](http://swirlstats.com/)

These are the basic commands within swirl:

<table>
<col width="44%" />
<col width="55%" />
<thead>
<tr class="header">
<th align="left">Name</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>bye()</p></td>
<td align="left"><p>Saves progress and exits</p></td>
</tr>
<tr class="even">
<td align="left"><p>info()</p></td>
<td align="left"><p>Display list of commands and their uses</p></td>
</tr>
<tr class="odd">
<td align="left"><p>nxt()</p></td>
<td align="left"><p>Continue the swirl lesson</p></td>
</tr>
<tr class="even">
<td align="left"><p>play()</p></td>
<td align="left"><p>Pauses swirl to go into &quot;sandbox&quot; mode</p></td>
</tr>
<tr class="odd">
<td align="left"><p>skip()</p></td>
<td align="left"><p>Skips current lesson question</p></td>
</tr>
</tbody>
</table>

Debugging Functions
-------------------

<table>
<col width="44%" />
<col width="55%" />
<thead>
<tr class="header">
<th align="left">Name</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>browser()</p></td>
<td align="left"><p>Suspends execution of a function and puts in debug mode</p></td>
</tr>
<tr class="even">
<td align="left"><p>debug()</p></td>
<td align="left"><p>Flags a function to &quot;step in&quot; line by line in debug mode</p></td>
</tr>
<tr class="odd">
<td align="left"><p>recover()</p></td>
<td align="left"><p>Modifies error behavior so you can look at function stack</p></td>
</tr>
<tr class="even">
<td align="left"><p>Rprof()</p></td>
<td align="left"><p>Starts R profiler</p></td>
</tr>
<tr class="odd">
<td align="left"><p>summaryRprof()</p></td>
<td align="left"><p>Summarizes output from R profiler</p></td>
</tr>
<tr class="even">
<td align="left"><p>trace()</p></td>
<td align="left"><p>Allows user to insert debugging code into a function</p></td>
</tr>
<tr class="odd">
<td align="left"><p>traceback()</p></td>
<td align="left"><p>Prints function stack to last call when error occurred</p></td>
</tr>
</tbody>
</table>



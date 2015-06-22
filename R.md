R Command Sheet 
===============================================================================

Basic R Commands
-------------------------------------------------------------------------------

+----------------------------------+------------------------------------------+
|Name                              | Description                              |
+==================================+==========================================+
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
|colnames() / rownames()           | Get or set a column/row for a matrix or  |
|                                  | dataframe                                |
+----------------------------------+------------------------------------------+
|complete.cases()                  | Returns a logical vector based on rows   |
|                                  | without missing values (NAs)             |
+----------------------------------+------------------------------------------+
|data()                            | Loads a data into the workspace          |
+----------------------------------+------------------------------------------+
|date()                            | Returns current system date              |
+----------------------------------+------------------------------------------+
|dir()                             | List files in the working directory      |
+----------------------------------+------------------------------------------+
|dir.create()                      | Creates a folder in the working directory|
|                                  | (Has recursive mode for subdirectories,  |
|                                  | which is off by default)                 |
+----------------------------------+------------------------------------------+
|environment(fun = NULL)           | Prints the environment of function _fun_ |
+----------------------------------+------------------------------------------+
|invisible(x)                      | Prevents the automatic printing of an    |
|                                  | object                                   |
+----------------------------------+------------------------------------------+
|library(package)                  | Loads an R package environment for use;  |
|                                  | _package_ is without quotes, and         |
|                                  | _help = package_ gives us documentation  |
+----------------------------------+------------------------------------------+
|ls()                              | List the objects in R's local workspace  |
+----------------------------------+------------------------------------------+



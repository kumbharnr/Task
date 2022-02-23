# Task

Problem Statement
The objective is to create a tool that acts as grep but for JSON log files . We will call this tool

1 2

json_grep.
The program should be invocable from the command line in the following manner:
json_grep PATTERN FILE
where PATTERN is the string that you need to search in every line of the FILE. By default (i.e
without any command line flags) json_grep should search in both keys and values of every
JSON object on each line. Apart from the default behavior of the tool, also implement the
following command line flags:
Command Line Options
-k Search only in keys of the JSON object
-v Search only in values of the JSON object
-x Ignore lines containing invalid JSON (see section below)
-i Case insensitive search
-c Show only the total number of lines matched instead of printing the matched lines
-d Print only the lines which DO not match the pattern provided
Note: All of the above flags can be combined with each other except the flags "-k" and "-v",
which are mutually exclusive.
Invalid JSON
If a line contains invalid JSON, print the following message and exit:
Invalid JSON on line number 23
Where 23 is the line number on which invalid JSON was encountered.
In case the user has passed -x option, then print no error and just continue from the next line.

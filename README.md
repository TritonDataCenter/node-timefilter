# timefilter - filter strings based on encoded timestamps

This module allows you to create a TimeStringFilter based on a strftime(3c)-like
format string and then use this object to filter out specific time intervals.
The prototypical example is that you have a directory tree organized by date
(e.g., YYYY/MM/DD/HH) and you want to scan the tree for files corresponding to a
certain range of dates.  Importantly, if you're scanning between 2014-05-03 and
2014-05-10, you want to eliminate the entire "2013" directory without descending
into it, so we need to be able to prune based on partial applications.

For example usage, see the [mprune
tool](https://github.com/joyent/manta-mprune).

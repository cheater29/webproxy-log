### Backup database ###

'Backup database' option can be activated at some points when you're uncertain of some actions (eg. when deleting records). When 'Backup database' option is selected, a copy of your database file will be made in WebProxy Log's configuration directory.


### Optimize ###

Optimization is a process which cleans your database of unneeded records (the deleted ones) and which defragments the database (can take a while on large databases).

### Insecure import ###
'Insecure import' is actually not so insecure and can't lead to database corruption. It's only a different approach when writing data to the database.

When you have this option turned off, WebProxy Log will wait for database to finish writing each line of data and then send new line of data to be written. That is not such a big deal if you have small log files (up to 2 MB daily), but on large log files (above 5 MB daily) the import process takes a log time to finish.

Therefore you can use 'insecure import' so WebProxy Log will send all the lines of data to the database without waiting each of them to be actually written. This 'insecure import' drastically speeds up the import process.
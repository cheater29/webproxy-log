### You'll need ###
  * configured [Logging environment](http://code.google.com/p/webproxy-log/wiki/Logging_environment)
  * log data for at least one day ([download zipped sample log](http://webproxy-log.googlecode.com/files/sample-log.zip))
  * WebProxy Log

### Importing logs ###
  * open WebProxy Log
  * go to 'File\Import logs'
  * click Import

All log files (any file that has 'log' extension) from pre-configured import location will then be read by WebProxy Log, reformatted and stored in local database. Imported log files, since they're stored in database, can be deleted or archived (recommended).

### Deleting records ###
  * open WebProxy Log
  * go to 'File\Delete records'
  * select whether to delete all records for certain user
  * select whether to delete certain web page records
  * once you've selected what to delete, press 'Delete' button

When you press the 'Delete' button, you are prompted to confirm deletion of n records found in the database.

When deleting records, you can backup database (this is done BEFORE actual deletion) and to optimize database after deletion.

Optimization is a process which cleans your database of unneeded records (the deleted ones) and which defragments the database (can take while on large databases).
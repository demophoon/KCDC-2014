Intro to MongoDB
================

Replication - You can setup the system to replicate data between systems. They 
also are setup in primary/secondary setup and if the primary fails for some
reason they other nodes vote on a new primary.

Shards - Like replication but data is distributed.

Quirks
------
- If you misspell anything mongo will happily create the record for you
- Check configs for installation, it is configured for production. You will
need to configure it for development databases
- Joins have to be in code
- It isn't strict about deleting rows but it is pretty strict about updating.

Design
------
- When designing a mongo database you need to look at usage patterns to get
the most out of it.
- Avoid using the dot (.) in the data.
- Key name length matters


vim: ft=markdown tw=80 sts=2 colorcolumn=80

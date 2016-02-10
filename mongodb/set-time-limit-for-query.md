# Set time limit for a query (2016-02-10)
The [`maxTimeMS`](https://docs.mongodb.org/v3.0/reference/method/cursor.maxTimeMS/) option can be used on a cursor to limit the maximum time that the query is allowed to run. If the query is interrupted when serving batches, the client will get the ready batches.

It's handy for pathlogical cases in text search, which may cause resource exahustion.

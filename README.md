# pg_objectlist ( Ubuntu 20.xx/ linux Executable)
utility to list all objects in PostgreSQL across the cluster.

usage: pg_objectlist [-h] --user USER --host HOST --port PORT [--file FILE] [--system-views SYSTEM_VIEWS]

Utility to collect object information across PG cluster. (c) DataXorg Data Services. version (1.0)

optional arguments:
  -h, --help            show this help message and exit
  --user USER           PostgreSQL super user.
  --host HOST           PostgreSQL host
  --port PORT           PostgreSQL port number
  --file FILE           output file name .csv
  --system-views SYSTEM_VIEWS ( Default False)
                        include system catalogs

Example: 

List on console : 
$ pg_objectlist --user=postgres --host=localhost --port=5434 --system-views=True


Save to .csv format : 
$ pg_objectlist --user=postgres --host=localhost --port=5434 --system-views=True --file=mydata.csv

Search object in all databases : 
$ pg_objectlist --user=postgres --host=localhost --port=5434 --system-views=True | grep userlogdetails_seq

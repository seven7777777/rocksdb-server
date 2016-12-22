# RocksDB-Server
A high performance [Redis](https://redis.io/) clone written in C using [RocksDB](http://rocksdb.org/) as a backend. 

## Supported commands

```
SET key value
GET key
DEL key
KEYS *
SCAN cursor [MATCH pattern] [COUNT count]
FLUSHDB
```

Any [Redis clients](https://redis.io/clients) should work.

## Building

Tested on Mac and Linux (Ubuntu), though should work on other platforms.
Please let me know if you run into build problems.

Requires `libtool` and `automake`.

Ubuntu users:
```
$ apt-get install build-esstential libtool automake
```

To build everything simply:

```
$ make
```

## Running

```
usage: ./rocksdb-server [-d data_path] [-p tcp_port] [--sync] [--inmem]
```
- `--inmem` -- The active dataset is stored in memory. 
- `--sync`  -- Execute fsync after every SET. More durable, but much slower.
- `-p`      -- TCP server port.
- `-d`      -- The database path.

## Contact
Josh Baker [@tidwall](http://twitter.com/tidwall)

## License
RocksDB-Server source code is available under the MIT [License](/LICENSE).
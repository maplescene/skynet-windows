## Build

For windows, open build/vs2013/skynet.sln and build all
You can use vs ide to debugging skynet

```
## Difference between offical skynet
1.sproto support real(double) field type
2.used event-select to simulate epoll
3.use socket api to simulate pipe()
4.hack read fd(0) for console input
```

For linux, install autoconf first for jemalloc

```
git clone https://github.com/cloudwu/skynet.git
cd skynet
make 'PLATFORM'  # PLATFORM can be linux, macosx, freebsd now
```

Or you can :

```
export PLAT=linux
make
```

For freeBSD , use gmake instead of make .

## Test

Run these in different console

```
./skynet examples/config	# Launch first skynet node  (Gate server) and a skynet-master (see config for standalone option)
./3rd/lua/lua examples/client.lua 	# Launch a client, and try to input hello.
```

## About Lua

Skynet now use a modify version of lua 5.3.1 (http://www.lua.org/ftp/lua-5.3.1.tar.gz) .

For detail : http://lua-users.org/lists/lua-l/2014-03/msg00489.html

You can also use the other official Lua version , edit the makefile by yourself .

## How To (in Chinese)

* Read Wiki https://github.com/cloudwu/skynet/wiki
* The FAQ in wiki https://github.com/cloudwu/skynet/wiki/FAQ

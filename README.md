# introduction
This is used for cross compile mtd-utils for p2020.
mtd-utils depends on some libs such as zlib, lzo and uuid.

# prepare sources

## mtd-utils
```
http://git.infradead.org/mtd-utils.git/tags

git clone git://git.infradead.org/mtd-utils.git
git checkout v1.4.0
```
## zlib
```
https://zlib.net/zlib-1.2.12.tar.gz
tar zxvf zlib-1.2.12.tar.gz
cd zlib-1.2.12
./configure
make

# install to cross compile directory

```

## lzo
```
http://www.oberhumer.com/opensource/lzo/download/lzo-2.10.tar.gz
tar zxvf lzo-2.10.tar.gz
cd lzo-2.10
./configure --host=powerpc
make

# delete ASSERT things for build
src/lzo_init.c
# delete conftest thins in configure file

# install to cross compile directory

```

## uuid
```
https://github.com/util-linux/util-linux.git
git clone https://github.com/util-linux/util-linux.git
# for proper version
git checkout xxxxx
./autogen.sh
./configure --disable-libblkid --host=powerpc
make

# install to cross compile directory

```

# Play with it


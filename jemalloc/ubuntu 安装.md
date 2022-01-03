# 下载

```sh
$ git clone https://github.com/jemalloc/jemalloc.git
```



# 安装

```sh
$ cd jemalloc
$ sudo apt install autoconf
$ ./autogen.sh
$ make dist
$ make
$ sudo make install
$ sudo bash
# echo /usr/local/lib >> /etc/ld.so.conf
# ldconfig
# exit
```



# 测试

```c
#include <stdio.h>
#include <jemalloc/jemalloc.h>
  
void jemalloc_test(int i)
{
        malloc(i*100);
}
 
int main(int argc, char **argv)
{
        int i;
        for(i=0;i<1000;i++)
        {
                jemalloc_test(i);
        }
        malloc_stats_print(NULL,NULL,NULL);
        return 0;
}
```

```sh
$ gcc jemalloc.c -o jemalloc -ljemalloc
$ ./jemalloc
```

或者

```sh
$ gcc jemalloc.c -o jemalloc -ljemalloc
$ LD_PRELOAD=/usr/local/lib/libjemalloc.so ./jemalloc
```


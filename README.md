# memalloc

memalloc is a simple memory allocator.

It implements <a href="http://man7.org/linux/man-pages/man3/free.3.html">malloc()</a>, <a href="http://man7.org/linux/man-pages/man3/free.3.html">calloc()</a>, <a href="http://man7.org/linux/man-pages/man3/free.3.html">realloc()</a> and <a href="http://man7.org/linux/man-pages/man3/free.3.html">free()</a>.

#### Compile and Run ####

```
gcc -o memalloc.so -fPIC -shared memalloc.c
```

The `-fPIC` and `-shared` options makes sure the compiled output has position-independent code and tells the linker to produce a shared object suitable for dynamic linking.


Now, if you run something like `ls`, it will use our memory allocator.
```
ls
memalloc.c		memalloc.so		README.md
```
or
```
vim memalloc.c
```

You can also run your own programs with this memory allocator.

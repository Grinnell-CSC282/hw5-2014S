A few useful macros....
### for-each
\#define foreach(item, array) \\
    for(int keep=1, \\
            count=0,\\
            size=sizeof (array)/sizeof *(array); \\
        count != size; \\
        keep=1, count++) \\
      for(item = (array)+count; keep; keep = !keep)

### Get array size
\#define ARRAY_SIZE(x) (sizeof(x) / sizeof((x)[0]))

References:
> array size: http://www.lainoox.com/tag/c-macro-examples/

> foreach: http://stackoverflow.com/questions/1772119/c-the-most-useful-user-made-c-macros-in-gcc-also-c99

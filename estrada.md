Here a dangerous use of macros:

#define ABS(a) (((a)<0) ? -(a) : (a))
#define ZSGN(a) (((a)<0) ? -1 : (a)>0 ? 1 : 0)

int func(int arg)
{
    return ABS(++arg);
}

int main(int argc, char** argv)
{
    printf("func(5) is %d\n", func(5));
    printf("func(-10) is %d\n", func(-10));
    return 0;
}

Citation:
http://www.gamedev.net/topic/175850-cool-macro-tricks/

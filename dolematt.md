###C macros from Kazlib

\#define get_top() ((struct except_stacknode \*) pthread_getspecific(top_key))

\#define set_top(T) (pthread_setspecific(top_key, (T)), (void)((T) == (struct except_stacknode \*) 0))

\#define set_catcher(C) (pthread_setspecific(uh_key, (void \*) (C)), (void)((C) == (void (\*)(except_t \*)) 0))

\#define set_alloc(A) (pthread_setspecific(alloc_key, (void \*) (A)), (void)((A) == (void \*(\*)(size_t)) 0))

\#define set_dealloc(D) (pthread_setspecific(dealloc_key, (void \*) (D)), (void)((D) == (void (\*)(void \*)) 0))

_Taken from [the Kazlib source code](http://git.savannah.gnu.org/cgit/kazlib.git/tree/except.c)_

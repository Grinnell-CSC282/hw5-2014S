###C macros from neovim

The first examples are toUpper and toLower for ASCII in macro form:

> <code>#define TOUPPPER_ASC(c) (((c) < 'a' || (c) > 'z') ? (c) : (c) - ('a' - 'A'))

> <code>#define TOLOWER_ASC(c) (((c) < 'A' || (c) > 'Z') ? (c) : (c) + ('a' - 'A'))

Another example of a macro checks to see if a line is empty and returns true if
it is:
> <code>#define lineempty(p) (*ml_get(p) == NUL)

More examples of macros can be found in the src/macros.h file of the neovim 
project [here](https://github.com/neovim/neovim?utm_source=explore-newsletter&utm_medium=email&utm_term=daily&utm_campaign=explore-email).

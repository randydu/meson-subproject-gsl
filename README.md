# Meson build for Microsoft Implemented GSL (Guidelines Support Library)

URL: 

- [Microsoft GSL: Guidelines Support Library](https://github.com/microsoft/GSL);
- [C++ Core Guidelines ](https://github.com/isocpp/CppCoreGuidelines);

The subfolder "src" is a clone of git repository of a specified release version. 
unit-tests are not built as part of the meson-build.

## Versions

The "revision" of gsl.wrap and the version of this meson-build project matches the embedded submodule GSL version as following:

Meson-Build |  GSL 
------------|-----------
1.0         | v4.0.0


## Usage

copy gsl.wrap to "subprojects" sub-folder of your main project directory.


in meson.build:

```
# import

gsl_dep = dependency('gsl')

# use
srcs = ['main.c', ...]

executable('test', srcs, dependencies: [gsl_dep, ...])

```

in main.c:

```c
#include <gsl/assert>

void foo(int x){
    Expects(x >= 0);
}
```




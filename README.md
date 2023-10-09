-compile lib

```bash
/usr/bin/g++ -shared -fPIC -o libexample.so example.cpp # -shared is to tell the compiler to create a shared library, -fPIC is to tell the compiler to create position independent code
```

-test lib

```bash
/usr/bin/g++ -o main main.cpp -L. -lexample -Wl,-rpath=./ # -Wl,-rpath=./ is to tell the linker to look for the library in the current directory
```
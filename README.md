# OCaml Graphics Demo

A simple project showcasing the `graphics` package of OCaml

## Building and Running This Project

To build, run

```
make clean && make
```

To run the test application, after building the project execute

```
./bin/demo
```

and follow the instructions on the screen.

## Installing OCaml Graphics

If you followed the initially provided instructions for installing the
OCaml infrastructure on your operating system, the project should be
working. Otherwise, follow the instructions below.

This project relies on OCaml's `graphics` package, which is somewhat
non-trivial to install, due to native system dependencies. Some
instructions on how make it work are provided below:

### Mac OS X

1. Install [XQuartz](https://www.xquartz.org/). 

2. Log-out from the system and log-in again.

3. After that, you will have to **re-install all packages** you have previously 
   installed via opam. For instance, first try

   ```
   opam switch
   ```

   If your version is, for instance `4.10.0`, next run

   ```
   opam switch reinstall 4.10.0
   ```

   It will take a while, as it re-builds all packages from scratch.
   
   The `graphics` package has been checked to work with OCaml
   `4.06.1`, `4.07.1`, and `4.10.0`.

4. Next, execute

   ```
   opam update; opam upgrade
   opam install graphics
   ```

   After that you should be able to build the project.

5. You might need to install `core`, and `batteries` via `opam` (using
   `opam install .`).
 

### Linux

1. Make sure that x11 window manager is installed (it comes as a part
   of most of the standard distributions).

2. Proceed to Step 3 for Mac OS X (above).

### Windows (Cygwin)

1. As it seems to be the case, x11 graphic interface is included into
   Cygwin (https://x.cygwin.com/).

2. Proceed to Step 3 for Mac OS X (above).


## More examples

You can find more examples of working with graphics in OCaml by
following
[this link](https://caml.inria.fr/pub/docs/oreilly-book/html/book-ora048.html) and by checking [this manuscript](https://caml.inria.fr/pub/docs/oreilly-book/pdf/chap5.pdf).






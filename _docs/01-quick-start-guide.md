---
layout: single
title:  "Quick start guide."
permalink: /docs/quick-start-guide/
excerpt: "Quick start guide: how to get started with Haskell for humans."
toc: true
---

The first thing to do will be to have a working Haskell environment. Depending on your operating system, it's not always straightforward. `GHC (Glasgow Haskell Compiler)` is the defacto compiler for Haskell, so it's the bare minimum to install.

The problem with only installing `GHC` is that soon, we will need to install dependencies, and the mess will begin. In this guide, I will always use a tool called `Stack` that will manage the dependencies mess for us. You can see it as an Haskell package manager that works. Everyone is using `Stack` so should you. Even for a very small project, I always setup a stack project. It's sometimes overkill, but it will give you a consistent way of working with your Haskell projects.

## Installing Stack

Go to the [installation guide of Stack](https://docs.haskellstack.org/en/stable/README/) and once it's done, try to setup a project:

```bash
stack new haskell-for-humans
cd haskell-for-humans
stack setup
stack build
stack exec haskell-for-humans-exe
```

If everything's fine, you're ready to go.

Below was my output of `stack build` and `stack exec haskell-for-humans-exe` the time of writing this guide. I was generating the code from the `/home/vjousse/usr/src/haskell/tmp` directory on my laptop. My version of `stack` was the `1.6.3`:

```
$ stack --version
Version 1.6.3, Git revision b27e629b8c4ce369e3b8273f04db193b060000db (5454 commits) x86_64 hpack-0.20.0
```
Output of `stack build`:

```
$ stack build
Building all executables for `haskell-for-humans' once. After a successful build of all of them, only specified executables will be rebuilt.
haskell-for-humans-0.1.0.0: configure (lib + exe)
Configuring haskell-for-humans-0.1.0.0...
haskell-for-humans-0.1.0.0: build (lib + exe)
Preprocessing library for haskell-for-humans-0.1.0.0..
Building library for haskell-for-humans-0.1.0.0..
[1 of 2] Compiling Lib              ( src/Lib.hs, .stack-work/dist/x86_64-linux-tinfo6-nopie/Cabal-2.0.1.0/build/Lib.o )
[2 of 2] Compiling Paths_haskell_for_humans ( .stack-work/dist/x86_64-linux-tinfo6-nopie/Cabal-2.0.1.0/build/autogen/Paths_haskell_for_humans.hs, .stack-work/dist/x86_64-linux-tinfo6-nopie/Cabal-2.0.1.0/build/Paths_haskell_for_humans.o )
Preprocessing executable 'haskell-for-humans-exe' for haskell-for-humans-0.1.0.0..
Building executable 'haskell-for-humans-exe' for haskell-for-humans-0.1.0.0..
[1 of 2] Compiling Main             ( app/Main.hs, .stack-work/dist/x86_64-linux-tinfo6-nopie/Cabal-2.0.1.0/build/haskell-for-humans-exe/haskell-for-humans-exe-tmp/Main.o )
[2 of 2] Compiling Paths_haskell_for_humans ( .stack-work/dist/x86_64-linux-tinfo6-nopie/Cabal-2.0.1.0/build/haskell-for-humans-exe/autogen/Paths_haskell_for_humans.hs, .stack-work/dist/x86_64-linux-tinfo6-nopie/Cabal-2.0.1.0/build/haskell-for-humans-exe/haskell-for-humans-exe-tmp/Paths_haskell_for_humans.o )
Linking .stack-work/dist/x86_64-linux-tinfo6-nopie/Cabal-2.0.1.0/build/haskell-for-humans-exe/haskell-for-humans-exe ...
haskell-for-humans-0.1.0.0: copy/register
Installing library in /home/vjousse/usr/src/haskell/tmp/haskell-for-humans/.stack-work/install/x86_64-linux-tinfo6-nopie/lts-10.2/8.2.2/lib/x86_64-linux-ghc-8.2.2/haskell-for-humans-0.1.0.0-7hqfH4sfHh79bkFf9fLDCO
Installing executable haskell-for-humans-exe in /home/vjousse/usr/src/haskell/tmp/haskell-for-humans/.stack-work/install/x86_64-linux-tinfo6-nopie/lts-10.2/8.2.2/bin
Registering library for haskell-for-humans-0.1.0.0..
```

Output of `stack exec haskell-for-humans-exe`:

```bash
$ stack exec haskell-for-humans-exe
someFunc
```

If you see `someFunc` displayed in your terminal, everything's fine, you can move on!

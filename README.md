# Introduction
This is an open-source implementation of coroutine. The fundamental idea is based on http://dunkels.com/adam/pt/. All codes are written in C.

The project provides a means to write light-weight tasks without creating multiple threads, by letting different tasks runing in the context of one thread. The benefits are
1. reducing overhead incurred by system context switch
2. avoiding error-prone lock coding usually needed in multi-thread programming

Asynchronous socket operations are provided as coroutine tasklets as well. This is to facilitate large-scale concurrent service programming.

The implementation is cross-platform, with Linux and MAC OS X currently supported.

# Build and Run
[shell] cd demo

Edit os.mk to make 'OS' either osx or linux, depending on the system you are working in.

[shell] make all

# Features
1. Asynchronous socket
2. Timers
3. Task yielding and scheduling

# TBD
1. A singly-linked list is needed
2. FIBER_SOCKET_XXX() further refactoring needed
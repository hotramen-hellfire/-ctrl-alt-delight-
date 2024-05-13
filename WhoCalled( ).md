 # Week3: WhoCalled( );
This week we'll closely inspect the abstraction provided by the kernel, i.e. how are userspace programs handled in MikeOS. How does the interface look for a user, how can he add and run programs of his own? 
To answer these questions, we'll try dissecting the implementations of ***syscalls*** in MikeOS, and then proceed to write one of our own.

>[BIBLE](https://mikeos.sourceforge.net/handbook-sysdev.html) (sysdev)
> This is quite an important text for you.
## Userspace Programs
By now you must be familiar with how commands are handled in MikeOS. Another set of programs you can run are the ones in the programs folder provided in MikeOS. For example, try `keyboard` or `adventure` as inputs in the cli.

 - Trace how the programs are being run, start tracing the assembly files from `cli.asm`.
 - Write a function, `os_say_hello` in `source/features/string.asm`.
 - Try writing a simple program in *nasm* in the programs folder named *meraprog.asm*, are you able to use:
	 - `os_print_string`in *meraprog.asm*? why?
	 - `os_say_hello`in *meraprog.asm*? why?
(Note: look at other `*.asm` userspace programs if you need help)
 - If you can explain the answers to these two questions, you have successfully understood the applications and needs for `syscalls`. Note that all functions in the OS code can be made to be user accessible. Similar to the *public*/ *private* constructs in C++ classes.
### ☮ Level 1
 - Try converting the `os_say_hello` function that you wrote into a syscall which can be used by userspace programs. Refer to the BIBLE shared.
 ### ☣ Level 2
 written by god?
 ### ☠ Level 3
think?

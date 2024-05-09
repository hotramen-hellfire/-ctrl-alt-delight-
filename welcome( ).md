# Week1: Welcome( );
*Written and Directed by Himanshu Gangwal.*   
**Hello :)**    
We will look at some of the very basic functions and implementations of an operating system.  However, before diving deep into the code, I would like you to know the basics of assembly. We are not going write programs in ***nasm*** but it would help you understand the code better. Apart for this the learning curve is not very steep if you know the workings of a CPU. (primitive knowledge about registers and memory access would suffice) * 

## M[i](https://github.com/mig-hub/mikeOS)k[e](https://github.com/mig-hub/mikeOS)O[S](https://github.com/mig-hub/mikeOS)
This is the best fit for our purpose, as it is quite ***BASIC*** (foreshadowing intended), in terms of features and can be extended easily due to its small kernel size which takes seconds to compile, as compared to most of the other alternatives. I started with xv6 initially but as expected it is much vaster (fyi, is a word) for the time that we have together.
### Installation
*It is better to try it yourself first, you'll have a great time trying to fix things, however this setup is quite ***BASIC***.*
 - Head onto the GitHub page of MikeOS and clone it onto a suitable location on your system. *It is always better to clear the `.git` folder after cloning. (OCD)*
 - You need to install the following dependencies as it is evident from the `build-linux.sh` script, viz. `nasm`, `mkisofs`, `mkdosfs`. Use your package manager to install these, you can use a quick google search for the package names. *Note: `mkisofs` and `mkdosfs` are a part of `cdrkit` and can be installed as `pacman -Sy cdrkit`  if `pacman` is your package manager.* (I am using [Mabox Linux](https://distrowatch.com/table.php?distribution=mabox) in case you were wondering)
 - Now you can run the `./build-linux.sh` which will create the required image.  *Read: `disk_images/README.TXT` for info on the image.*
 - Now we need to install `qemu-system-i386` as required to emulate the OS image. `sudo apt install qemu-system` or `sudo pacman -Sy qemu-full`, will suffice.
 - Now run `./test-linux.sh`, it should give an `-soundhw` error. You can simply remove `-soundhw pcspk` from the command in the script, as believe me listening to ***Kendrick*** is much better. *Fix-> [see here](https://www.reddit.com/r/qemu_kvm/comments/xte6kq/how_do_i_use_pcspk_now_that_soundhw_is_deprecated/). You can also remove the unidentified file system warning-> [here](https://unix.stackexchange.com/questions/276480/booting-a-raw-disk-image-in-qemu).*

 *`qemu-system-i386 -audiodev pa,id=audio0 -machine pcspk-audiodev=audio0 -drive format=raw,file=disk_images/mikeos.flp` is the final command that I am using.* We're done with the set up :)

#todo _ nasm and into message?

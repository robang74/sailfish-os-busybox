## BusyBox for SailFish OS

The busybox .config and RPM .spec for SailFish OS

### Rationale

This fork is focused in producing a fully feature static busybox and the dynamic has been kept, just in case.

Both .config files has been modified for this aim and aligned as much as possible. 

The original configs has been kept for reference.

---

> :warning: WARNING (obsolete since 1.36.1-git2-raf2)
>
> Unless you know exactly what you are doing, avoid to install the RPMs produced by this project because there is a good chance
> they will brick your system in such a way you will need to reflash it unless you have a rescue image and the skills to undo
> the changes made by the RPMs installation. For this reason the versioning report the postfix `-raf1` to let know that it is not the
> busybox you have installed nor anyone from Jolla. Since the `-raf2`, this issue is almost addressesed, read below.

> :heavy_exclamation_mark: ATTENTION (addressed since 1.36.1-git2-raf3)
>
> Only the statically linked busybox uses preferably its applets. This changes the behaviour of your system because even if the `PATH`
> for executable search is correctly set as usual in your shell enviroment, the command prompted into one of the busybox shells are
> going to refers to the busybox applets. Moreover - if you set a cross-compiling enviroment and therefore you change  the `PATH` in
> order to run the target architecture tools as prefered - they will run correctly unless the command name will not overloaded by a
> busybox applet. It is a important feature for recovering a bricked system but also a trick that it can confuse end-users and the
> apps developers. The alternative is to install the dynimically linked busybox which has not this feature but if the system is
> briked bad also the shared libraries needed to let busybox can be unavailable and this is main reason because the statically
> linked is a fully stand-alone executable.

> :information_source: DONE (since 1.36.1-git2-raf2)
>
> A fully features busybox would create a lot of links during the building process and there is a good chance that they will be
> reported into the RPMs which will refuse to install because the conflicts, in the best case. This situation shall be fixed in
> the future because it can be useful to have a static fully features busybox installed into the regular root filesystem even if
> the system would continue to use the installed binaries: a busybox with many applets without their links.
>
> Fortunately the RPM build failed and log out all the links created but not expected. Those links has been added in a single RPM
> package named `symlinks-others` which brings within it `Provides: deprecated()` and `Conflicts: busybox` limitations that hopefully
> will prevent anyone to install it by an accident. Unless `--force` is used by default but in such case they deserve it.

---

### Conclusion

This fork is for SFOS refactoring and it should be employed within this specific framework, only. 

If you like to play with and/or learning about embedded systems on mobile devices, you are welcome into the club.

If you brick your mobile device and you fear to loose your precious data because you never did a backup of them, wait before crying. 
You will be not left behind: you also will be welcomed, as 💲upporter of the club :wink:.

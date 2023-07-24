## BusyBox for SailFish OS

The busybox .config and RPM .spec for SailFish OS

### Rationale

This fork is focused in producing a fully feature static busybox and the dynamic has been kept, just in case.

Both .config files has been modified for this aim and aligned as much as possible. 

The original configs has been kept for reference.

---

> :warning: WARNING
>
> Unless you know exactly what you are doing, avoid to install the RPMs produced by this project because there is a good chance
> they will brick your system in such a way you will need to reflash it unless you have a rescue image and the skills to undo
> the changes made by the RPMs installation. For this reason the versioning report the postfix `-raf1` to let know that it is not the
> busybox you have installed nor anyone from Jolla.  

> :heavy_exclamation_mark: ATTENTION
>
> Both version static and dynamic linked build by this project use preferably their applets. This changes the behaviour of your system
> because even if your `PATH` for executable search is correctly set as usual in your shell enviroment, the command prompted into one
> of the busybox shells are going to refers to the applets. Moreover - if you set a cross-compiling enviroment and therefore you change
> the `PATH` in order to run the target architecture tools as prefered - they will run correctly unless the command name will not
> overloaded by a busybox applet. It is a important feature for recovering a system but also a trick that it can confuse end-users and
> and UI apps developrs which are not aware about this internal behaviour of the busybox.

> :information_source: TODO
>
> A fully features busybox would create a lot of links during the building process and there is a good chance that they will be
> reported into the RPMs which will refuse to install because the conflicts, in the best case. This situation shall be fixed in
> the future because it can be useful to have a static fully features busybox installed into the regular root filesystem even if
> the system would continue to use the installed binaries: busybox with applets without links.

---

### Conclusion

This fork is for SFOS refactoring and it should be employed within this specific framework, only. 

If you like to play with and/or learning about embedded systems on mobile devices, you are welcome into the club.

If you brick your mobile device and you fear to loose your precious data because you never did a backup of them, wait before crying. 
You will be not left behind: you also will be welcomed, as 💲upporter of the club :wink:.

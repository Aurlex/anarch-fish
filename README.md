# anarch-fish
(dubious) fish shell demake of https://github.com/selirra/anarch

## DANGER
- I do not claim any responsibility for anything that happens to your device from using this. I am honestly shocked I didn't brick my phone. <3
- If you don't use `start_arch.fish`, or it crashes, ensure that you run `unmount_arch.fish` after you're done, otherwise you might end up with a bricked handset.
  - I have not verified this for, for obvious reasons.
- !!YOU MUST!! ensure that the chroot is unmounted before deleting root/ or disk.img, or your partitions are will cry.
- If you want to delete `disk.img`, you should run `losetup -a | grep /full/path/to/disk.img | awk '{print $1}' | tr -d :` to check if any loopback devices are stil mounted before doing so. If they are, restart your phone, or find a way to unmount them.

## How To Use
1. Root your android device
2. Install Termux
3. Install the `tsu` package to access root in termux
4. Run this script as root (very carefully)
     - Please look at the contents first; this is a hacky script. Not a polished product. Do not trust it. <br> <br>
   ```fish
   $~ tsu
   $~ fish install_arch.fish
   ```
6. Follow the process in the script
7. Use `start_arch.fish` to use the chroot.

# If it breaks, feel free to submit a fix
##### But please don't expect too much of me

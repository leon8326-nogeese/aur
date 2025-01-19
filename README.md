# Nogeese AUR
AUR for Nogeese Linux.
## Can i get this AUR on Arch Linux?
Maybe your here from the mirror's README, but you can!

But like the nogeese repo, it was made for Nogeese Linux.

If you want it follow these steps:

Open "/etc/pacman.conf" in a text editor and

Add this line:

```
[aur]
Server = https://raw.githubusercontent.com/leon8326-nogeese/aur/main/aur
SigLevel = TrustAll
```

## For the official mirror click [here](https://github.com/leon8326-nogeese/mirror/blob/main/README.md).

## As a developer, how can i upload a new package on this AUR?
Fork this AUR, and download the .db and .files in the aur folder you want to have your package on, for this example we will add yay.

Make sure it is a separate new directory with all the .db and .files in it.

Now add the *.pkg.tar or *.pkg.tar.zst package onto the same directory.

In this example it will be yay-*-x86_64.pkg.tar.zst.

Paste this package into the same directory as all the .db and .files.

Then run this command in the same directory:

```
repo-add aur.db.tar.gz $package-*-$arch(.pkg.tar/.pkg.tar.zst)
```

In this example it will be:

```
repo-add aur.db.tar.gz yay-*-x86_64.pkg.tar.zst
```

And then delete ALL the .db and .files in the aur directory on the fork you created on github.

And in the same directory click + > Upload files and drag and drop the .pkg.tar/.pkg.tar.zst and all the .db and .files, then click "Commit changes".

Go to the home page of the fork and click "Contribute" follow instrustion on the screen, and wait... your package should be approved.

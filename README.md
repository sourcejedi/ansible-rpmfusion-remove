# rpmfusion__impl #

This role is not to be invoked directly.  It provides both the code and documentation for `sourcejedi.rpmfusion-free` and
`sourcejedi.rpmfusion-nonfree`, as available on ansible galaxy.


## rpmfusion-free

Enable the [RPM Fusion](https://rpmfusion.org/) "free" software repository.


## rpmfusion-nonfree

Enable the [RPM Fusion](https://rpmfusion.org/) "nonfree" software repository.
This role enables the "free" repository at the same time, as it may be required by software in "nonfree".


## Requirements

Fedora Linux


## Package Signing Keys

This role will verify the known fingerprints of RPM Fusion package signing keys, inspired by Dockerfile best practices.  If you like, you can cross-check the [current fingerprints](https://rpmfusion.org/keys) from the RPM Fusion website.

Once installed, updates to the RPM Fusion keys will be delivered through the package manager as per usual.

We'll also have to update the keys in the role, when new releases become available.  This is easy to keep up with for releases, because RPM Fusion provides keys two releases in advance (for branched/rawhide?).


## License

The role itself is licensed GPLv3, please open an issue if this creates any problem.

There are two RPM Fusion repositories you can enable:

* one named "free" for Open Source Software (as defined by the [Fedora Licensing Guidelines](https://fedoraproject.org/wiki/Licensing:Main?rd=Licensing)) which can't be included in Fedora because it might be patent encumbered in the US.
* one named "nonfree" for non-free software, that is everything else which can't be in free; this includes software with public available source-code that has "no commercial use"-like restrictions.
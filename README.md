# rpmfusion_remove #

Remove the [RPM Fusion](https://rpmfusion.org/) "free" or "nonfree" software repository.

This is slightly less friendly than my installer roles.

Note "the nonfree repository depends on the free repository."
This role will not stop you from removing "free" and leaving "nonfree" installed.
That could theoretically cause updates to fail, so please don't do it.

This role is designed so you can start by running it in check mode.
It will report the list of RPM Fusion packages which will be removed.
Notice that if you run the role twice to remove both repositories, you
will need to look at two different tasks to see all of the packages which
will be removed.


## Requirements

Fedora Linux


## Variables

* `repo` - which repo to remove - "free" or "nonfree".


## License

The role itself is licensed GPLv3.  Please open an issue if this creates any problem.


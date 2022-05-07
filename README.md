# img_mount
This is a script that is used for mounting Images for inspection and editing purposes. It handles standard filesystems and LVM partitions as well. The raw_msdos_mount function will work on a Linux image that is a single partition. Anything with more partitions than that it is not guaranteed to work. For Linux images with more that one partition the raw_linux_mount function should be used, as long as there are no LVM partitions in the image (though those should be caught by the script and handled as such).

# config
This is a configuration file that sets names and values

# install
This creates the image file based on the values in config

# run
This runs the image in a qemu vm. It both runs the original iso file and the image after it has been fully built.
## multi-threading
To enable multi-threading add the argument options:
```
-smp cores=2,threads=1,sockets=1
```
The values of each argument should be changed to fit the needs of the system being ran.

## TODO:
Handle btrfs filesystems

Add a cleanup function

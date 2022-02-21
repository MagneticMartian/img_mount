# img_mount
This is a script that is used for mounting Images for inspection and editing purposes. It handles standard filesystems and LVM partitions as well. The raw_msdos_mount function will work on a Linux image that is a single partition. Anything with more partitions than that it is not guaranteed to work. For Linux images with more that one partition the raw_linux_mount function should be used, as long as there are no LVM partitions in the image (though those should be caught by the script and handled as such).

## TODO:
Handle btrfs filesystems

Add a cleanup function

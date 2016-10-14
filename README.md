# ubuntu-classic-image

## Introduction

This project creates a filesystem image for a Raspberry Pi2 (support for other devices is coming soon). You can download an already-built system image for various SBCs at http://bluehorizon.network.

Related Projects:

* `anax` (http://github.com/open-horizon/anax): The client control application in the Horizon system
* `bluehorizon-snap` (http://github.com/open-horizon/bluehorizon-snap): A Ubuntu Snappy bundling of the complete Horizon client components

## Operations

### Create SD card image

#### Preconditions

* Execution on an armhf device (often we build on Odroid xu4 or C2 SBCs)
* You must have the module `dm_multipath` loaded and `kpartx`, `parted`, `zip`, `unzip`, `fsarchiver`, and other common GNU tools installed

#### Steps

* Execute `make sd-image`; the resulting image will be written to /mnt/extra. If you'd like to change the output location, execute `(export IMAGE_OUTPUT_DIR=/tmp/; make -e sd-image)`.

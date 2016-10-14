# ubuntu-classic-image

## Introduction

This project creates a filesystem image for a Raspberry Pi3 and Pi2 using unofficial Ubuntu PPAs, or Pi2 only using official PPAs. You can download an already-built system image for various SBCs at http://bluehorizon.network.

Related Projects:

* `anax` (http://github.com/open-horizon/anax): The client control application in the Horizon system
* `bluehorizon-snap` (http://github.com/open-horizon/bluehorizon-snap): A Ubuntu Snappy bundling of the complete Horizon client components

## Operations

### Create SD card image

#### Preconditions

* Execution on an armhf device (often we build on Odroid XU4 or Odroid C2 SBCs)
* You must have the following Linux modules loaded:
  * `dm_multipath`
* You must have the following tools available (among common GNU tools):
  * `kpartx`
  * `parted`
  * `zip`
  * `unzip`
  * `wget`

#### Steps

* Execute `make pi2-sd-image` to make an official, Pi2-only image or `make pi3-sd-image` to make a Pi3 and Pi2 compatible image. The resulting image will be written to /mnt/extra. If you'd like to change the output location, execute `(export IMAGE_OUTPUT_DIR=/tmp/; make -e pi3-sd-image)`.

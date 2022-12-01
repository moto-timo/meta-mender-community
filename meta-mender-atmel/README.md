# meta-mender-atmel

Mender integration for atmel based boards

The supported and tested boards are:

 - [Microchip SAMA5d27-SOM1-EK1](https://hub.mender.io/t/microchip-sama5d27-som1-ek1/127)
 - [Microchip SAMA5D3 Xplained](https://hub.mender.io/t/microchip-sama5d3-xplained/194)


Visit the individual board links above for more information on status of the
integration and more detailed instructions on how to build and use images
together with Mender for the mentioned boards.

## Dependencies

This layer depends on:

```
URI: https://github.com/linux4sam/meta-atmel
branch: kirkstone
revision: HEAD
```

```
URI: https://github.com/mendersoftware/meta-mender.git
layers: meta-mender-core
branch: kirkstone
revision: HEAD
```

## Quick start

The following commands will setup the environment and allow you to build images
that have Mender integrated.


```
mkdir mender-atmel && cd mender-atmel
repo init -u https://github.com/mendersoftware/meta-mender-community \
          -m meta-mender-atmel/scripts/manifest-atmel.xml \
          -b kirkstone
repo sync
source setup-environment atmel
MACHINE=sama5d27-som1-ek-sd bitbake core-image-base
```



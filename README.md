![](https://img.shields.io/github/actions/workflow/status/daixtrose/how-to-use-docker-for-copperspice/docker-copperspice-compile-and-install-image.yml?style=plastic)

# How to use Docker for Copperspice

## Disclaimer

:warning: :gear: :hammer_and_wrench: This is merely a concept study in alpha stage! Give me some time to get things straight.

## Summary

This is a demo on how to use Docker for the development of GUI apps with [CopperSpice](https://github.com/copperspice). 

This repository mainly consists of Docker recipes and [GitHub Actions](https://github.com/features/actions) scripts (aka the GitHub CI/CD pipeline) for the creation of containererized build environments. 

If you are only interested in a specific build environment, then you can download it from the packages region on the right hand side.

It is designed in such a way that one can fork this repository. The CI files will upload container images to the GitHub container registry of repository owner. 

## Standing on the Shoulders of Giants

This repository includes build environments for the Raspberry Pi 4 modeled after the [instructions provided on the CopperSpice webpage](https://www.copperspice.com/docs/cs_overview/build-pi.html). All my gratitude to [Barbara Geller](@bgeller) and [Ansel Sermersheim](@agserm) for helping me sort these things out - and to provide [CopperSpice](https://www.copperspice.com) in the first place!  

The Dockerfile build system is based on [Bernd Doser](@BerndDoser)'s ingenious build scripts published in [docker-devel-env](https://github.com/BrainTwister/docker-devel-env). 





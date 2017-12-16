# EasyElectrumBuilder
Build releasable Windows/macOS/Linux/Android binaries for Electrum clones for your favorite coins

EasyElectrum is derived from [EasyGitian](https://github.com/mazaclub/EasyGitianBuilder} and [mazaclub's electurm release packager](https://github.com/guruvam/mazaclub-release} 

This project will provide the ability to build Electrum in a 100% clean and fresh environment on each build OS, and produce binaries in as reproducible way as is practical with a Python application. 

EasyElectrum will attempt to install Vagrant and Virtualbox if you don't have them, and then will proceed to constructing 
VMs needed to build an electrum derived package.

Due to Apple licensing restrictions, there are no ready downloadadble VMs from the official source (apple), so EasyElectrum must create it's own. EasyElectrum will build VMs with Yosemite, ElCapitan, Sierra, and High Sierra, per your preference. You must furnish the original "Install macOS Sierra.app" in your /Applications, ~/Applications, or ~/Downloads directories and EasyElectrum will build a bootable ISO, and install macOS automaticall in a VM for you. 

EasyElectrum will build additional VMs for processing the Windows, Linux and Android builds. VM base images are downloaded from official sources, and provisioned by Vagrant for building Electrum.

macOS builds technically require building on Apple hardware. While this is not a strict requirement (macOS VMs can run on non-Apple hardware under linux or Windows) but this configuration is not officially supported. 

EasyElectrum will build for Windows Linux and Android on any OS (except Android!) 


EasyElectrum uses pyinstaller to create Windows, macOS, and Linux builds, and buildozer to perform Android builds. 

EasyElectrum will include scripts to provision and launch each builder VM from. your host OS, and the necessary configuration to retrieve the build artifacts and release files. It should be suitable for use in your CI workflow.

## Requirements

EasyElectrum v0.1.0 will be built against Electrum, Electrum-GRS, and Tate (ElectruMAZA), in that order. 
  - v0.0.1 Electrum for Bitcoin (original Source) - **Version 3.0 and above ONLY**
  - v0.0.2 Electrum for Groestlcoin - supports C Extension hash modules (supports any coin needing this) 
  - v0.0.3 Tate (ElectuMAZA) - potentially support for pre 3.0 upstream code and python2.7


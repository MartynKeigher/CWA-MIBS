# Automate MIBS

### What is this Repo for? 

The purposes of this repo is to maintain a 'ready-to-use' drop-in set of MIBS that can be used with ConnectWise Automate.

Currently, the process of importing MIBS can be 'tedious' due to nature of how MIBS work (in general).


### How will this project work?

- The initial commit of this repo (aka: Release v1.0) is the default 'out-of the box' set of MIB files, that come with ConnectWise Automate **2020.1**.

- Each future release of this repo, from that point on, will contain more MIBS that, once verified of a successful MIB load (in Automate), can be used for Network Monitoring within the ConnectWise Automate product.

- Newly added MIBS will be documented with each release.


### High-level workflow

1. New MIBS will be added to the project via a 'develop' branch.
2. These MIBs will then be loaded into Automate to ensure that the loading of the MIB folder is still successful.
3. If the loading of the MIBS returns errors, then they will be modified until a successful loading can occur.
4. Upon a successful MIB load, the contents of the dev branch, will then be merged to the 'master' branch.
5. Major 'master' updates will incur a new release build. (While a 'release' is not a technical requirement for functionality... why not?)


### What denotes a successful 'loading of mibs'?

When the Automate Control Center is launched, part of the process is to read the MIBS that are in the 'LTShare\MIBS\RFC' folder. The contents of this folder are then synced to 'C:\ProgramData\LabTech Client\MIBS\RFC' on the machine launching the Control Center. **__This is a one-way sync__**. *From: LTShare To: ProgramData*. The Command console shows the progress of the MIBs loading from the ProgramData folder and reports the finished state. A successful loading of mibs reports like this:

![Command Console](https://i.imgur.com/40ozdG6.png)

Error messages vary based on which MIB(s) failed to import:

*TODO: Add pic of failed import here!*


### How do I use this repo?

After downloading a release of this project, simply REPLACE the contents of LTShare\MIBS\RFC with what is provided in the release. 

This repo, and the maintaining of it, is a personal project and in no way officially supported by ConnectWise. 


### How can I contribute?

*TODO: Add How to PR stuff here!*

---
While every effort is made to ensure that each release will give 100% success rate, please [report an issue](https://github.com/MartynKeigher/Automate-MIBS/issues) if you come across any! 

Please note: This repo, and the maintaining of it, is a personal project and is not officially supported by ConnectWise.

Thank you.

://mk

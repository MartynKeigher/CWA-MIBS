# CW Automate MIBS

### What is this Repo for? 

The purposes of this repo is to maintain a 'ready-to-use' drop-in set of MIBS that can be used with ConnectWise Automate.

Currently, the process of importing MIBS can be 'tedious' due to nature of how MIBS work (in general).


### How will this project work?

- The initial commit of this repo (aka: Release v1.0) is the default 'out-of the box' set of MIB files, that came with ConnectWise Automate **2020.1**.

- Each future release of this repo, from that point on, will contain more MIBS that, once verified of a successful MIB load (in Automate), can be used for Network Monitoring within the ConnectWise Automate product.

- Newly added MIBS will be [documented here](https://github.com/MartynKeigher/Automate-MIBS/releases) with each release.


### High-level workflow

1. New MIBS will be added to the project via a 'develop' branch.
2. These MIBs will then be loaded into Automate to ensure that the loading of the MIB folder is still successful.
3. If the loading of the MIBS returns errors, then they will be modified until a successful loading can occur.
4. Upon a successful MIB load, the contents of the dev branch, will then be merged to the 'master' branch.
5. Major 'master' updates will incur a new release build. (While a 'release' is not a technical requirement for functionality... why not?)


### What denotes a successful 'loading of mibs'?

When the Automate Control Center is launched, part of the process is to read the MIBS that are in the 'LTShare\MIBS\RFC' folder. The contents of this folder are then synced to 'C:\ProgramData\LabTech Client\MIBS\RFC' on the machine launching the Control Center. **__This is a one-way sync__**. *From: LTShare To: ProgramData*. The Command console shows the progress of the MIBs loading from the ProgramData folder and reports the finished state.

A successful loading of MIBs reports like this:

![Command Console](https://i.imgur.com/40ozdG6.png)

Error messages vary based on which MIB(s) failed to import. An unsuccessful loading of MIBs reports like this:

![Command Console](https://i.imgur.com/r8tyDwb.jpg)


### How do I use this repo?

After downloading a release of this project,

- Close the Control Center. (Thick client).

- Replace the contents of \\LTShare\MIBS\RFC with the contents of this project's latest release.

- Delete 2 folders on the server\workstation you are running the Control Center from:

    - C:\ProgramData\LabTech Client

    - C:\ProgramData\LabTech Plugins

- Restart the 'ConnectWise File Service' service on the Automate Server.

- Re-Open the Control Center & log in.

- The NEW MIBS will now load successfully. 


This repo, and the maintaining of it, is a personal project and in no way officially supported by ConnectWise. 


### How can I contribute?
This is only an overview - you might need to research some parts of this. 

You will need a basic understanding of git including: 
 - clone (making a copy of a repository)
 - pull (get commited changes)
 - commit (make changes)
 - push (send changes)
I'll let you look those up yourself. Git can be a complex system so try not to get distracted beyond knowing what those commands do because for this they're all you've going to need for this. 

You will need to have a Github account, then Fork this repo (look in top right of this page) which makes a copy of it in your account.

Clone _your_ repo to your computer and make all the changes you want and test them. Commit all your change to git and push them to your Github repo.  

AFTER you've tested and are SURE the code in your Github repo works properly then come back to this repo (https://github.com/MartynKeigher/CWA-MIBS) and create a Pull Request (aka PR - see https://docs.github.com/en/github/collaborating-with-issues-and-pull-requests/about-pull-requests) from the Github web interface. This will notify Martyn that you're submitting changes to be incorporated into the his repo, and make it easy for him to review and merge them in.  

---
While every effort is made to ensure that each release will give 100% success rate, please [report an issue](https://github.com/MartynKeigher/Automate-MIBS/issues) if you come across any! 

Please note: This repo, and the maintaining of it, is a personal project and is not officially supported by ConnectWise.

Thank you.

://mk

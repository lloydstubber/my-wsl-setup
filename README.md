# My WSL Setup for Development
Quick rundown on my current setup  Windows Subsystem for Linux.


After a few headaches with running the Git Bash on Windows I’ve decided to move over the WSL for all development purposes. I’m very new to Linux so this is a very top-level overview so feel free to submit any changes.

Here’s a breakdown of how I got up and running below:



### Download & Install the WSL
- Follow the very thorough instructions [here](https://msdn.microsoft.com/en-au/commandline/wsl/install_guide)



### Get your terminal looking pretty
- Download Hyper.js [here](https://hyper.is/)
  - I went with the 'hypernasa' theme



### Automatically open in Bash
- Open up Hyper and type `Ctrl` + `,`
- Scroll down to shell and change it to `C:\\Windows\\System32\\bash.exe`



### Install Git
- Run this `sudo apt update`
- Then run `sudo apt install git`



### Setup a SSH key and link to your Github
- Follow the Linux steps [here](https://help.github.com/articles/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent/#platform-linux) to create a key and add it to your SSH agent
- Then type `cat ~/.ssh/id_rsa.pub`
- Copy your key from the terminal and paste it into your Github keys



### Install Node Version Manager
- Follow the instructions [here](https://gist.github.com/micahgodbolt/8b9a338c8bab7bc147975646ea20826c) which will get you running on Node/NPM and can easily roll-back versions to suit.
  - With running NPM/Gulp I had issues with version 8 of Node. So I rolled back to version 5 and that fixed NPM install errors.



### Install Gulp CLI
- Follow the Gulp docs [here](https://github.com/gulpjs/gulp/blob/master/docs/getting-started.md).


---

### Notes
- I had trouble with Node/NPM/Gulp before realising Ubuntu won’t automatically upgrade from 14.04 to 16.04 - as mentioned in this [article](https://blogs.msdn.microsoft.com/commandline/2017/04/11/windows-10-creators-update-whats-new-in-bashwsl-windows-console/).
  - If you’re in the same boat, upgrade via these [instructions](https://help.ubuntu.com/lts/serverguide/installing-upgrading.html).
- I also had trouble with older versions of Windows 10 not liking Gulp via the WSL - inotify and socket issues. Make sure you're running on the Creators Update or Insiders Program versions.

# Latex_CV
Documenting Latex setup and templates for generating a CV

## Environment
    Ubuntu 18.04
    Texmaker
  
Using the quickbuild function of Texmaker, was able to aggregate results pdfs into a single pdf.

First template I wanted to try is [link](https://www.latextemplates.com/template/wenneker-resume-cv).
This would not compile, but the issue is resolved in a single step with the following.

    sudo apt install texlive-full


### Dead end - starting at whatever texLive was already installed
First template I wanted to try is [link](https://www.latextemplates.com/template/wenneker-resume-cv).

The issue was XCharter.sty not found. How do I install packages to latex?

Using tlmgr apparently. To first setup tlmgr, if it is has never been used before, do the following.

    tlmgr init-usertree
    
Then add the package

    sudo tlmgr Install xcharter
    /usr/bin/tlmgr: Please install xzdec and try again.
    sudo apt install xzdec
    
Complaint is that the tlmgr is too old. Workaround is

    sudo tlmgr option repository ftp://tug.org/historic/systems/texlive/2017/tlnet-final
    
Now the compilation of the CV example fails with:
    
    ! Package fontenc Error: Encoding file `t2aenc.def' not found.

This is turning into a slow game of slogging through dependencies, so we abandon it.

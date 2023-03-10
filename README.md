# github_udemy
Quick Install on Mac OS X Notes
Introduction
This document provides a quick listing of the tools needed and basic install instructions for each -- which is used throughout this course. Before you get started installing all the tools and software for this course, there are a few basic requirements. After that, I provide the -+general instructions foversr each tool used. Since this page is designed to aide the "get to the point" crowd, I keep my instructions as brief as possible.

In order to support the most recent version of Mac OS X available, these instructions were tested using 10.10 or higher.

Getting Started and Common Tools
Admin Rights

You need to have Administrator rights to your system. Most modern versions of Mac OS X come with several "flavors" of user accounts -- only Administrators can install software.

Security Tweaks

Modern versions of Mac OS X come with a default setting to disallow installation of software from unsigned applications or unknown third-parties. If you experience problems installing software, you may need to allow the most liberal setting for installing software from within System Preferences > Security & Privacy.

Google Chrome

Optional.

I use Google Chrome for most of my courses. A few years ago, I would have strongly recommended or border-lined required the use of Chrome. However, most modern versions of all common browsers are adequate -- although the software engineer in me still prefers Chrome. For those wanting to follow along as closely as possible, install and use Chrome during this course. However, this is an optional step now, but I include it for completeness.

Install for Mac OS X
Go to the Google Chrome Desktop page at https://www.google.com/chrome/browser/desktop
Click on the Download Chrome button
Accept the Terms of Service agreement (after reading, of course)
Follow the instructions through the install process
Git (from Apple)
Required.

Git is the source control tool used in this course. Apple provides Git with Xcode, but it is also available via the Developer Command Line Tools by Apple.

Install

Open Terminal and type:

git version
If Git responds with a version number, then Git is already installed. Otherwise, Mac OS will prompt for the installation of the Command Line Tools or Xcode. Either is fine, but choose Command Line Tools for a much faster download and install.

Configure Git

Git requires your name and email address before any real work can be done. It is best to just configure Git from the start.

git config --global user.name "Your Name"
git config --global user.email "your.email@your-place.com"
TextMate 2
Optional.

Mac OS comes with a text editor called TextEdit, but it isn't very powerful and many IT professionals prefer something more. I use a free program called TextMate 2 for most of my Mac based courses. If you are happy with TextEdit, then this step is optional.

Install

Download TextMate 2 from http://macromates.com/download
Expand the archive and copy the TextMate app into the Applications stack
Open TextMate from the Applications stack
Terminal Configuration

With TextMate 2 open:

Go to Preferences
Go to the Terminal Tab
Click the Install button to setup the mate command
Git Integration

Open Terminal and issue the command:

git config core.editor "mate -w"
Then test it out by:

git config --global -e
P4Merge on Mac
P4Merge for Mac is a visual comparsion and merge resolution tool that integrates well with Git.

Install

Download P4Merge: Visual Merge Client from https://www.perforce.com/downloads/helix#clients
Once the installer image has finished downloading, open the image volume.
Run only the P4V client
Git Integration

Now, let's integrate P4Merge with Git. You'll need to know where P4Merge is installed on your system -- which is normally under /Applications. With the next series of commands, you may need to modify them slightly to fit your system.

Configure P4Merge as Diff Tool in Git:

git config --global diff.tool p4merge
git config --global difftool.p4merge.path "/Applications/p4merge.app/Contents/MacOS/p4merge"
git config --global difftool.prompt false
Configure P4Merge as Merge Tool in Git:

git config --global merge.tool p4merge
git config --global mergetool.p4merge.path "/Applications/p4merge.app/Contents/MacOS/p4merge"
git config --global mergetool.prompt false

# Summary
The iMac G4 PowerPC 1GHz is a 32bit PowerPC-based Macintosh that was released by Apple near the turn of the century. It
contains a built-in monitor that is attached via a shiny chrome boom arm attached to the base unit which is a matte
white half-dome.

This is also know as the "sunflower iMac".

The last release of Apple's operating system supported is 10.5.8, codenamed "OSX Leopard".

## Connectivity
Apple's Safari browser is now so old that it is not functional due to the HTTPS encryption algorithms it supports (or
better yet, DOESN'T support). It would be beneficial to have a working browser, otherwise everything that needs to be
downloaded locally before getting Tigerbrew (Homebrew port) installed will need to be done on another system and
transferred to the iMac.

A stable version of the browser TenFourFox, a port of FireFox, can be found in the Wayback Machine. The purpose of using
archive.org is that it will (hopefully) never change causing link rot.

[TenFourFox Browser](https://archive.org/details/ten-four-fox-final)

This .dmg file will need to be downloaded on another machine and then transferred to the iMac via SCP or Bonjour.

## Developer Tools
Before installing anything, the iMac needs to have Xcode installed, however Apple requires a developer account before
they give access to any old Xcode images. Thankfully the Wayback Machine has old copies of Xcode available for download
for free. 

[Old Xcode Install Images](https://archive.org/details/xcode_old_versions)

Under Mac OSX Disk Images the file named xcode_3.1.4_2809_developerdvd.dmg is what is needed to be using the latest
Xcode for Max OSX 10.5.8.

After Xcode is installed, just open it one time to make sure the command line tools aren't blocked by needing to
acknowledge a user agreement first.

## Package Manager
To make a Macintosh functional for any System Administrator, Scientist, Engineer, or anyone else who wants to take full
control of their Mac, a terminal-based package manager must be installed. This will give the Mac access to regular linux
packages that Apple refuses to put into their base system. For modern Macs, this tool is called Homebrew, but
unfortunately it does not support the PowerPC architecture. However, a group of software developers has ported Homebrew
to run on the PowerPC architecture.

[Tigerbrew on GitHub](https://github.com/mistydemeo/tigerbrew)

It will be necessary to download the Tigerbrew install script through the TenFoxFour browser as the Terminal HTTPS
functions are still not usable due to how old the protocols are and the lack of terminal tools.

Once the script is downloaded the work in the terminal on the iMac can be started. Installing Tigerbrew using ruby can
be performed with:

```bash
ruby path/to/install
```

After Tigerbrew is installed the first thing to run is brew help and brew doctor to finalize the install and see the
state of the package manager. After that installing packages will work just as it does with Homebrew on a modern system.

![Running brew help takes some time](https://github.com/rdustinb/Vintage-Computing/blob/b9ddd78a5c629196eba4ca6f5f3ec601d0fa830f/iMac%20G4%20PowerPC/images/brewhelp.png "Brew Help")

Using NeoFetch shows just how limited the old Apple Terminal is with colors. I think it only supports 8 colors.

![NeoFetch output on iMac G4 PowerPC](https://github.com/rdustinb/Vintage-Computing/blob/b9ddd78a5c629196eba4ca6f5f3ec601d0fa830f/iMac%20G4%20PowerPC/images/neofetch.png "NeoFetch")

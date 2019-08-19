## <p align="center">![Screenshot](https://nr1.nu/emagnet/previews/emagnet_oldmovi.gif)

<a href="https://github.com/wuseman/EMAGNET">
<img src="https://img.shields.io/github/languages/top/wuseman/emagnet.svg?color=magenta&label=Bash%2FShell"></a>

<a href="https://github.com/wuseman/EMAGNET/issues?q=is%3Aissue+is%3Aclosed">
<img src="https://img.shields.io/github/issues-closed/wuseman/emagnet.svg?color=light&label=Closed%20Issues"></a>
  
<a href="https://github.com/wuseman/EMAGNET/issues">
<img src="https://img.shields.io/github/issues-raw/wuseman/emagnet.svg?color=orange&label=Open%20Issues"></a>
 
<img src="https://img.shields.io/github/last-commit/wuseman/emagnet.svg?color=darkmagenta&label=Latest%20Commit">

<a href="https://twitter.com/wuseman1">
 <img src="https://img.shields.io/website/https/nr1.nu.svg?down_color=darkred&down_message=DOWN&label=Nr1.nu%2Femagnet&up_message=UP">
    <img src="https://img.shields.io/github/license/wuseman/emagnet.svg?color=blue&label=License"></a></a></a>
</a>
</p>

| Current Version    |  Released      | News                            | Tested On                          |
| :----------------- | :------------- | :-------------------------------- | :----------------------------------|
| `3.4`              |  2019-08-04    |  Full support on android devices, no root required    | Linux                               |


Emagnet is a very powerful tool for it's purpose wich is to capture email addresses and passwords from leaked databases uploaded on pastebin. It's almost impossible to find leaked passwords when they are out of list on pastebin.com. Either they have been deleted by pastebin's techs or the uploads is just one in the crowd. To be honest it's easier to find a needle in a haystack then find outdated uploads on pastebin with the data we want to collect. 

### Demo
![Screenshot](.preview/emagnet-preview.gif)

### Filtered email addresses:
![Screenshot](.preview/emagnet-log.png)
* This video has been made of an unknown user so don't blame me, got it in my inbox. Thanks for the video!

### Get Started On Linux/MacOSX

    git clone https://github.com/wuseman/emagnet
    cd emagnet
    chmod +x emagnet*
    .
    ./emagnet --emagnet

###  Get Started On Windows 10

Please visit my installation [wiki](https://github.com/wuseman/EMAGNET/wiki/Installation) for more info (includes a video)

### Get started on Android via Termux

* Download termux from play store [here](https://play.google.com/store/apps/details?id=com.termux&hl=en_US)
    
When termux has been installed open termux and run below commands, you can copy and paste:

     pkg update
     pkg upgrade -y
     pkg install wget curl git -y
     git clone https://github.com/wuseman/emagnet

     cd emagnet
     bash emagnet --emagnet

### How to get VPN running with emagnet..

* Create a folder in /etc/openvpn with your providers name, for example hidemyass:

       mkdir -p /etc/openvpn/hidemyass

* Download the configuration files from the providers homepage and unzip them in above folder. 

* Now name vpn files as below: 

       /etc/openvpn/hidemyass/hidemyass-nz.ovpn 
       /etc/openvpn/hidemyass/hidemyass-no.ovpn
       /etc/openvpn/hidemyass/hidemyass-se.ovpn
       /etc/openvpn/hidemyass/hidemyass-nl.ovpn
       ..... And so on..


* Don't forget to add your login file if necessary: 

      for files in /etc/openvpn/provider; do echo "auth-user-pass login.txt" >> $files; done


See VPNCOUNTRYS in emagnet.conf for what countries is available as default and how emagnet reading the files. 
You can of course edit the countrys to anything else but feel free to get it working on your own then.

If you have two providers or even three as I do, just do exactly as above then but edit VPNPROVIDER2 and 3 for your other provider and same with countries name them after VPNCOUNTRYS2 and 3. Now you can scrape pastebin every second if you want since you will change ip asap you have been banned but please don't do that. Use it with common sense.

### How to get started with brute forcer for spotify:

* On GNU/Linux Gentoo wich is the supported distro for emagnet, just do as following:

      emerge --ask eselect-repository
      eselect repository enable palmer
      eix-sync;eix-update
      emerge --ask =dev-libs/libspotify-12.1.51
      emerge --ask media-libs/portaudio

* Now you are ready to brute force spotify accounts:

      bash emagnet --bruteforce spotify

* On Ubuntu/Kali/Debian:

      wget -q -O - https://apt.mopidy.com/mopidy.gpg | sudo apt-key add -
      wget -q -O /etc/apt/sources.list.d/mopidy.list https://apt.mopidy.com/stretch.list
      sudo apt-get update
      sudo apt-get install libspotify12 libspotify-dev libportaudio

* Now you are ready to brute force spotify accounts:

      bash emagnet --bruteforce spotify

### Wiki Sections:

- [About](https://github.com/wuseman/EMAGNET/wiki/ABOUT) - 
_How everything started._

- [Previews](https://github.com/wuseman/EMAGNET/wiki/ABOUT) - 
_Previews for all Emagnet features can be found here._

- [Faq](https://github.com/wuseman/EMAGNET/wiki/FAQ) - 
_How to grab your visa card if it has been leaked. Also get answers why we not using TOR._

- [Installation](https://github.com/wuseman/EMAGNET/wiki/INSTALLATION) - 
_Video preview for how to get started on windows_

- [Tips & Tricks](https://github.com/wuseman/EMAGNET/wiki) - 
_How To Find your facebook credenticals, if it has been leaked._

### System requirements

- Bash     - Find more info about _bash_ [here](https://www.gnu.org/software/bash/)
- Wget     - Find more info about _wget_ [here](https://www.gnu.org/software/wget/)
- Curl     - Find more info about _curl_ [here](https://github.com/curl/curl)

#### BBC NEWS: ["Pastebin: Running the site where hackers publicise their attacks"](https://www.bbc.com/news/technology-17524822) 
- Emagnet is your best friend for get the leaks, you will be the first viewer on every paste but it of course matters of  the time you have set ;-)

## Changelog

[Versions changelog](CHANGELOG.md).

## Authors: 

* **wuseman <wuseman@nr1.nu\>** 

## License

This project is licensed under the GNU General Public License v3.0 - see the [LICENSE.md](LICENSE.md) file for details

### Contact

  If you have problems, questions, ideas or suggestions please contact me on *_wuseman@nr1.nu_  - For faster contact visit freenode irc network or the webchat and type '/msg wuseman hi!' in the input bar and I will reply you ASAP I will see the message.
  
  Enter Freenodes network via your own client 'chat.freenode.com:+6697 or use their new web client [here](https://webchat.freenode.net/)

### Notice

Attacking different kinds of accounts via emagnet that you have not been granted or allowed to attack is strictly prohibited and it breaks the law. The punishment is hard and you can even get into prison in some countries just for trying to attack for intrusion. With this said, it's *important* that all users is aware of this and when you have cloned or downloaded it's fully up to every user to take responsibility over their own actions. wuseman cannot be held responsible for the actions of any user, all users using Emagnet on their own responsibility. 

Developer: "All my previews where a brute force attack has been done is under controlling forms with 100% fully permissions by the owners. If you have any questions about this then you are welcome to contact me or the owner."

### Haters Gonna Hate

If you are one of these who dislikes _EMAGNET_ and believe the program has been developed for a reason that would break the law then I am not interested in taking part of your opinions, keep them for _yourself_! Emagnet does **NOT** leak any data at all either to the developer(s) or anyone else. No statistics at all to track any user so if you want to contact me for ask who it might was who downloaded emagnet a specific date is completely useless since i really have no idea, and to be honest I don't care.

Feel free to read the history about emagnet [here](https://github.com/wuseman/EMAGNET/wiki/About) and how everything started about this project.

#### Development of emagnet is active and is updated frequently, please use the latest version if you report issues/bugs.

### Emagnet is a private project since 2015 and was released in June @ 2018, to be continued. 


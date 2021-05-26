# Customize PowerShell With Oh-my-posh and WSL with Oh-my-zsh on Windows 10 

<img src=/Captures/4.png alt="Windows 10 Explorer"/>

## Starting 🚀

_I share this windows 10 settings, which I hope you ❤️ if you´re a .NET developer, in the resources folder you will find backgrounds, logos and fonts for your terminal and your wallpaper, the font Cascadia Code for PowerShell and
Droid Sans Mono is for WSL, in the Terminal Windows folder is the .JSON configuration file of my terminal, enjoy it_


### Prerequisites 📋

_What you need to customize your terminal_

```
1.-Download this repository from Zip or Git

2.-Upgrading to Windows 10 20H2.

3.-Windows Terminal from the Microsoft Store

4.-PowerShell from the Microsoft Store

5.-Git for Windows and Git for WSL

6.-Debian-based Linux distributions from the Microsoft Store

7.-SUSE-bases Linux distributions from the Microsoft Store

8.-Love and peace

```

### Installing prerequisites 🔧

_[Windows Terminal](https://www.microsoft.com/es-mx/p/windows-terminal/9n0dx20hk701?activetab=pivot:overviewtab)_


<img src=/Captures/5.png alt="Windows Terminal"/>

_[PowerShell](https://www.microsoft.com/es-mx/p/powershell/9mz1snwt0n5d?activetab=pivot:overviewtab)_

<img src=/Captures/6.png alt="PowerShell 7"/>

_Linux distributions: [OpenSUSE Leap 15.2](https://www.microsoft.com/es-mx/p/opensuse-leap-152/9mzd0n9z4m4h?activetab=pivot:overviewtab), [Ubuntu 20.04](https://www.microsoft.com/es-mx/p/ubuntu-2004-lts/9n6svws3rx71?activetab=pivot:overviewtab), [Debian 10](https://www.microsoft.com/es-mx/p/debian/9msvkqc78pk6?activetab=pivot:overviewtab) and [Kali](https://www.microsoft.com/es-mx/p/kali-linux/9pkr34tncv07?activetab=pivot:overviewtab/)_

<img src=/Captures/7.png alt="Linux distributions"/>


## Windows Terminal 🖥

### Oh-my-posh on PowerShell 🔧

_A series of step-by-step examples that tells you what to run to customize PowerShell on your Terminal_

_Once downloaded the Windows Terminal and this repository copies the fonts from folders to Windows Fonts, remembers Cascadia Code for PowerShell and DroidSansMono for WSL_

<img src=/Captures/8.png alt="Fonts"/>

_Run a PowerShell Terminal as an administrator and then install Oh-my-posh in PowerShell with the following commands; remember to decline for trusting the source:_

```
Install-Module posh-git -Scope CurrentUser
```
```
Install-Module oh-my-posh -Scope CurrentUser
```

_Import the modules into your PowerShell profile_

```
Import-Module posh-git
Import-Module oh-my-posh
Set-PoshPrompt -Theme Aliens
```

_Remove restrictions on modules_

```
Set Execution-Policy Unrestricted
```
<img src=/Captures/9.png alt="ProfilePS"/>



_In the resources folder, leave the JSON settings of my profile, use it for the general configuration of the terminal, for the configuration of the different shells, CLI and command prompt that you have, and for the powershell and WSL color schemes. Compare it to your JSON settings and don't complicate your life copy and paste._

<img src=/Captures/11.png alt="SchemesPS"/>
<img src=/Captures/12.png alt="SchemesPS"/>

_If all went well, the result is..._ 

<img src=/Captures/13.png alt="Oh-my-posh"/>

### Oh-my-zsh on Windows Subsystem for Linux ⚙️

_A series of step-by-step examples that tells you what to run to customize Windows Subsystem for Linux on your terminal, if you installed the DroidSansMono fonts you already have the first step, the next step is to copy the logos from the resources folder._

_If you work on local disk C, this should be the path where to paste the logos:_

```
C:\Users\youuser\AppData\Local\Packages\Microsoft.WindowsTerminal_8wekyb3d8bbwe\RoamingState
```

<img src=/Captures/16.png alt="Logos"/>

_In this tutorial we will work with openSUSE, but you can do this in Debian based distribution , using APT as a package manager should not see problems._

_Update the system and install zsh and oh-my-zsh, I leave you here the commands:_

```
sudo zypper update
```
```
sudo zypper install zsh
```
_Clone and accept that zsh is your default shell:_
```
sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

<img src=/Captures/17.png alt="zsh"/>

_Clone the powerlevel10k theme:_

```
git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/themes/powerlevel10k
```

_Open the zsh configuration file:_

```
vim ~/.zshrc
```

_Change the "ruselnoseque" theme to:_

```
powerlevel10k/powerlevel10k
```

<img src=/Captures/18.png alt="vim"/>

_Now close and reopen your terminal, when you open it you will see a screen to configure your theme powerlevel10k, it´s basic english, here is more explain to do, if you want to re-adjust the theme type this command:_

```
p10k configure
```

_Finally set up the OpenSUSE profile in the windows terminal settings, customize to your liking, this is mine_ 

<img src=/Captures/19.png alt="SUSE"/>


_One more thing, to install it in Debian based distributions you have to use the apt package manager, with the same process_ 

```
sudo apt update
```
```
sudo apt install zsh -y
```
<img src=/Captures/20.png alt="Ubuntu"/>
<img src=/Captures/21.png alt="Debian"/>


# Prework for .NET developers that use Python on Windows and Linux ✌😁 🖥

<img src=/Captures/23.png alt="Tecnologies"/>


## Docker on WSL(Ubuntu-20.04)

_A standard software package (known as a "container") groups an application's code with the associated libraries and configuration files, along with the dependencies required for the application to run. This allows developers and IT professionals to deploy applications seamlessly across all environments_

_First we need to upgrade to windows subsystem for linux to version 2 (Incorporates a complete Linux Kernel built by Microsoft itself and released with the windows 2004 version... build X)_

_With the following command we list the installed Linux distributions_

```
wsl -l
```

_Now we convert WSL 1 to WSL 2 with the following command by adding the distro name with parameter 2_

```
wsl --set-version (distro) 2
```

_With this command we list the distros with their version_

```
wsl -l -v
```

<img src=/Captures/24.png alt="Conversion"/>

_Now download and [install Docker Desktop](https://hub.docker.com/editions/community/docker-ce-desktop-windows/) or use winget package manager from powershell (with WSL 2 you don't need to have Windows 10 pro or enterprise to use it)_

```
winget install docker
```
<img src=/Captures/25.png alt="Winget"/>


_In the installation make sure that Docker accesses WSL and at the end of the installation make sure that the Docker engine is WSL-enabled and uses the default distro, if not refreshes and marks the distribution to use, as in the following image_

<img src=/Captures/26.png alt="Docker Desktop"/>

_Finally check that everything went well, open a new terminal with the Linux distro configured for Docker and run the following image_

```
docker run hello-world
```

<img src=/Captures/27.png alt="Hello World"/>


## Build with: 🛠️

* [Fluent Design](https://www.microsoft.com/design/fluent/#/) - Fluent Design System
* [Windows Terminal](https://docs.microsoft.com/en-us/windows/terminal/) - Windows Terminal Docs
* [.NET](https://docs.microsoft.com/en-us/dotnet/core/install/linux-ubuntu#2004-) - .NET 5 on Ubuntu 20.04
* [Docker](https://docs.docker.com/docker-for-windows/install-windows-home/) - Docker Desktop on Windows Home
* [Oh-my-posh](https://github.com/JanDeDobbeleer/oh-my-posh) - Oh-my-posh repository | check this out, for more themes
* [Oh-my-zsh](https://ohmyz.sh/) - zsh website 
* [Powerline10k](https://github.com/romkatv/powerlevel10k) - Powerline10k Theme
* [Cascadia Code](https://www.hanselman.com/) - Cascadia Code PL Fonts
* [DroidSansMono](https://www.nerdfonts.com/) - DroidSansMono Fonts
* [Blog of Scott Hanselman](https://www.hanselman.com/) - This guy is GREAT 😵
* [The digital life](https://www.the-digital-life.com/en/) - Check this out


## Expressions of gratitude

* Thank you for reviewing this repo-tutorial to customize windows 10 with Fluent Design for .NET Developers 🤓
* Expect more tutorials of .NET

---
⌨️ With ❤️ By [Jonas-Lara](https://github.com/Jonas-Lara) 😊

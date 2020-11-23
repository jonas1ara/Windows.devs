# Customize Windows 10 With Fluent Design for .NET Developers

<img src=/Captures/01.png alt="Windows 10"/>
<img src=/Captures/02.png alt="Windows 10 Home"/>
<img src=/Captures/03.png alt="Windows 10 Terminal"/>
<img src=/Captures/04.png alt="Windows 10 Explorer"/>

## Starting 🚀

_I share this windows 10 settings, which I hope you ❤️ if you´re a .NET developer, in the resources folder you will find backgrounds, logos and fonts for your terminal and your wallpaper, the font Cascadia Code for PowerShell and
Droid Sans Mono is for WSL, in the Terminal Windows folder is the .JSON configuration file of my terminal, enjoy it_


### Prerequisites 📋

_What you need to customize your terminal_

```
1.-Upgrading to Windows 10 20H2, if you're using WSL you already enjoy this update

2.-Windows Terminal(Preview) from the Microsoft Store

3.-PowerShell Preview from the Microsoft Store

4.-Files Preview from the Microsoft Store

5.-Git for Windows and Git for WSL

6.-Debian-based Linux distributions from the Microsoft Store

7.-Love and peace

```

### Installing prerequisites 🔧

_Windows Terminal (Preview), Why preview? Because_

<img src=/Captures/Terminal.png alt="MS Terminal"/>

_PowerShell Preview from the Microsoft Store, because it comes from the Microsoft Store and not from a repository_

<img src=/Captures/PowerShell.png alt="MS Terminal"/>

_Files Preview, This is a very very special, because Windows 10 needs revamped file explorer_

<img src=/Captures/Files.png alt="MS Terminal"/>


## Windows Terminal 🖥

### Oh-my-posh on PowerShell 🔧

_A series of step-by-step examples that tells you what to run to customize PowerShell on your Terminal_

_Once downloaded the Windows Terminal and this repository copies the fonts from the compressed folders (Obvious unzips first) in Windows Fonts remembers Cascadia Code PL for PowerShell and DroidSansMono for WSL_

<img src=/Captures/Fonts.png alt="Fonts"/>

_Then install Oh-my-posh in PowerShell, with the following commands; remember to decline for trusting the source_

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
Set-Theme Paradox
```
<img src=/Captures/PROFILES$.png alt="ProfilePS"/>

_Run a PowerShell Terminal as an administrator, to remove restrictions on modules_

```
Set Execution-Policy Unrestricted
```

<img src=/Captures/Set.png alt="Set"/>

_In the Windows-Terminal folder I leave you two sections of json files, one for the complete configuration of terminal windows and one for color themes, for each color scheme attached a shot as an example, in tastes are broken genres, it is my customization does not have to like you, I invite you to copy the profiles you need and then play with the color scheme_

<img src=/Captures/ConfPS.png alt="ConfigPS"/>

<img src=/Captures/esquemasPS.png alt="SchemesPS"/>

_If all went well, the result is..._ 

<img src=/Captures/windowsPS.png alt="MT"/>
<img src=/Captures/windowsCMD.png alt="MT"/>
<img src=/Captures/windowsAzure.png alt="MT"/>

### Oh-my-zsh en Windows Subsystem for Linux ⚙️

_A series of step-by-step examples that tells you what to run to customize Windows Subsystem for Linux on your terminal, if you installed the DroidSansMono fonts you already have the first step, the next step is to copy the logos from the resources folder_

_If you work on local disk C, this should be the path where to paste the logos_

```
C:\Users\youuser\AppData\Local\Packages\Microsoft.WindowsTerminal_8wekyb3d8bbwe\RoamingState
```

<img src=/Captures/Logos.png alt="Logos"/>

_In this tutorial we will work with Ubuntu, but you can do this in Debian and Kali, since they use APT as package manager and bash as predete rminada shell should not see differences_

_After downloading the distro from the Microsoft Store and entering a user and password, update the system and install zsh and oh-my-zsh, I leave you here the commas, accept that zsh is your default shell_

```
sudo apt update
```
```
sudo apt install zsh -y
```
```
sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

_Accept that zsh is your default shell and install the powerline10k theme with the following comando_


```
git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/themes/powerlevel10k
```


_Open the zsh configuration file_

```
vim ~/.zshrc
```

_Change the "ruselnoseque" theme to:_

```
powerlevel10k/powerlevel10k
```

<img src=/Captures/ct.png alt="CP"/>

_Now close and reopen your terminal, when you open it you will see a screen to configure your theme powerlevel10k, it is basic English, here is more explain to do, if you want to re-adjust the theme type this command:_

```
p10k configure
```

_Finally set up the Ubuntu profile in the windows terminal settings, either way I leave you my JSON files to give you an idea_ 

<img src=/Captures/windowsUbuntu.png alt="Ubuntu"/>
<img src=/Captures/windowsDebian.png alt="Debian"/>
<img src=/Captures/windowsKali.png alt="Kali"/>


## Build with: 🛠️

* [Fluent Design] (https://www.microsoft.com/design/fluent/#/) - Fluent Design System
* [Oh-my-posh](https://github.com/JanDeDobbeleer/oh-my-posh) - Oh-my-posh repository | check this out, for more themes
* [Oh-my-zsh](https://ohmyz.sh/) - zsh website 
* [Powerline10k](https://github.com/romkatv/powerlevel10k) - Powerline10k Theme
* [Cascadia Code](https://www.hanselman.com/) - Cascadia Code PL Fonts
* [DroidSansMono](https://www.nerdfonts.com/) - DroidSansMono Fonts
* [Windows Terminal](https://docs.microsoft.com/en-us/windows/terminal/) - Windows Terminal Microsoft Docs
* [Blog of Scott Hanselman](https://www.hanselman.com/) - This guy is GREAT 😵
* [The digital life](https://www.the-digital-life.com/en/) - Check this out


## Expressions of gratitude

* Thank you for reviewing this repo-tutorial to customize windows 10 with Fluent Design for .NET Developers 🤓
* Expect more tutorials of .NET

---
⌨️ With ❤️ By [Jonas-Lara](https://github.com/Jonas-Lara) 😊

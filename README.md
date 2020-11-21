# Customize Windows 10 With Fluent Design for .NET Developers

<img src=/Captures/01.png alt="Windows 10"/>
<img src=/Captures/02.png alt="Windows 10 Home"/>
<img src=/Captures/03.png alt="Windows 10 Terminal"/>
<img src=/Captures/04.png alt="Windows 10 Explorer"/>

## Starting 🚀

_I share this windows 10 settings, which I hope you ❤️ if you´re a .NET developer, in the resources folder you will find backgrounds, logos and fonts for your terminal and your wallpaper, the font Cascadia Code for PowerShell and
Droid Sans Mono is for WSL, in the Terminal Windows folder is the .JSON configuration file of my terminal, enjoy it. _


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

### Oh-my-posh en PowerShell 🔧

_Una serie de ejemplos paso a paso que te dice lo que debes ejecutar para personalizar powershell en tu terminal_

_Una ve descargados la terminal de windows y este repositorio copia las fuentes de las carpetas comprimidas(Obvio descomprime primero) en Fonts de windows recuerda Cascadia Code PL para powershell y DroidSansMono para WSL_

<img src=/Capturas/Fonts.png alt="Fonts"/>

_Despues instala Oh-my-posh en PowerShell, con los siguientes comandos; recuerda declinar por confiar en la fuente_

```
Install-Module posh-git -Scope CurrentUser
```
```
Install-Module oh-my-posh -Scope CurrentUser
```

_Importa los módulos a tu perfil de PowerShell, SUSTITUYE adria por tu usuario_

```
Import-Module posh-git
Import-Module oh-my-posh
Set-Theme Paradox
```
<img src=/Capturas/PROFILE$.png alt="ProfilePS"/>

_Corre una shell de PowerShell como administrador, para quitar las restricciones a los módulos_

```
Set Execution-Policy Unrestricted
```

<img src=/Capturas/Set.png alt="Set"/>

_En la carpeta Windows-Terminal te dejo dos secciones de archivos json, uno para la configuración completa de windows terminal y otro por temas de colores, por cada esquema de color anexo una toma como ejemplo, en gustos se rompen generos, es mi personalización no tiene porque gustarte, te invito a que copies los perfiles que necesites y posteriormente jugar con el esquema de colores_

<img src=/Capturas/ConfPS.png alt="ConfigPS"/>

<img src=/Capturas/esquemasPS.png alt="SchemesPS"/>

_Si todo salio bien, el resultado es..._ 

<img src=/Capturas/1.png alt="PS"/>
<img src=/Capturas/2.png alt="PS"/>

### Oh-my-zsh en Windows Subsystem for Linux ⚙️

_Una serie de ejemplos paso a paso que te dice lo que debes ejecutar para personalizar powershell en tu terminal, si instalaste las fuentes DroidSansMono ya llevas el primer paso, el siguiente es copiar los logos(O los que tu prefieras) de la carpeta recursos_

_Si trabajas en el disco local C, esta deberia ser la ruta donde pegar los logos_

```
C:\Users\youuser\AppData\Local\Packages\Microsoft.WindowsTerminal_8wekyb3d8bbwe\RoamingState
```

<img src=/Capturas/Copialogos.png alt="Logos"/>

_En este tutorial vamos a trabajar con Ubuntu, pero puedes hacer esto en Debian y Kali, dado que usan APT como administrador de paquetes y bash como shell predeterminada no debe a ver diferencias_

_El primer paso es descargas una distro de Linux desde la Microsoft Store e introducir un usuario y constraseña, despues actualizar el sistema e instalar zsh y oh-my-zsh, te dejo aquí los comandos, acepta que zsh sea tu shell predeterminada._

```
sudo apt update
```
```
sudo apt install zsh -y
```
```
sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

_Acepta que zsh sea tu shell predeterminada e instala el tema powerline10k con el siguiente comando_


```
git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/themes/powerlevel10k
```


_Si no hiciste cosas, la pantalla que muestra es la siguiente:_

<img src=/Capturas/quesiverga.png alt="QSV"/>

_Cambia el tema de zsh, escribe_

```
vim ~/.zshrc
```

_Cambia el tema "russelnoseque" por:_

```
powerlevel10k/powerlevel10k
```

<img src=/Capturas/changepower.png alt="CP"/>

_Ahora cierra y vuelve a abrir tu terminal, cuando la abras te aparecera una pantalla para configurar tu tema powerlevel10k, es inglés básico, aquí esta de mas explicar que hacer, si quieres volver a ajustar el tema escribe este comando_

```
p10k configure
```

_Para finalizar configura el perfil de Ubuntu en los ajsutes de la terminal de windows, de cualquier manera te dejo mis archivos JSON para que te des una idea_ 

<img src=/Capturas/4.png alt="Ubuntu"/>
<img src=/Capturas/5.png alt="Debian"/>
<img src=/Capturas/6.png alt="Kali"/>


## Construido con 🛠️

* [Oh-my-posh](https://github.com/JanDeDobbeleer/oh-my-posh) - Respositorio Oh-my-posh | ojo aqui, hay mas temas
* [Oh-my-zsh](https://ohmyz.sh/) - página web de zsh 
* [Powerline10k](https://github.com/romkatv/powerlevel10k) - Tema powerline10k
* [Cascadia Code](https://www.hanselman.com/) - Fuente Cascadia Code PL
* [DroidSansMono](https://www.nerdfonts.com/) - Fuente DroidSansMono
* [Windows Terminal](https://docs.microsoft.com/en-us/windows/terminal/) - Documentación oficial de la terminal de windows
* [Blog of Scott Hanselman](https://www.hanselman.com/) - Este tipo es un crack 😵
* [The digital life](https://www.the-digital-life.com/en/) - Checa el blog de mi colega


## Expresiones de Gratitud 🎁

* Gracias por visitar este repositorio para personalizar tu terminal en windows 🤓
* Espera nuevos tutoriales sobre el ecosistema .NET

---
⌨️ con ❤️ por [Jonas-Lara](https://github.com/Jonas-Lara) 😊

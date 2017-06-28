

**Table of Contents**  

- [Installing Skype](#installing-skype)



<a name="installing-skype"></a>
# Installing Skype

Skype is a popular messaging and telephony client. It isn't open source and the license prohibits redistribution however it is possible to install it using Korora's package manager or from the command line using dnf.

The RPMFusion repository provides a Local Package Factory package that downloads and installs Skype and its required dependencies. Skype is only available as a i686 package but will run on 64 bit systems.

To install type

```
sudo dnf install lpf-skype
```

When it is installed run lpf-skype from the menu. It will handle the download and installation of Skype. Just follow the instructions on the screen. You will be asked for your password to authorise installation and also need to click OK in a confirmation screen.

When it is complete Skype will appear on the Internet section of your menu.



**Table of Contents**  

- [Installation](#installation)
- [Remove the Screensaver (Optional)](#remove-the-screensaver-optional)
- [Xfce Specific Configuration](#xfce-specific-configuration)
    - [Xfce Power Manager](#xfce-power-manager)
    - [Xfce Xflock4 and Whisker Menu](#xfce-xflock4-and-whisker-menu)



Many people dislike XScreensaver and its ugly unlock screen but keep it for the security of its screenlocking. Korora includes Xscreensaver with Xfce. Xscreensaver provides both the screensaver graphics and screenlocking for security. Screensaving isn't needed these days with modern monitors. It is a relic from the distant past of CRT monitors. You can disable the screensaving so it just blanks the screen. But you still have the ugly Xscreensaver screen to type your password. There is a better way.

<a name="installation"></a>
### Installation
First install light-locker. `sudo dnf install light-locker` is all that is needed. A restart is required.

<a name="remove-the-screensaver-optional"></a>
### Remove the Screensaver (Optional)
With Light Locker installed the screensaver is no longer needed so it can be removed with `sudo dnf remove xscreensaver*`

When returning to a computer with the screen locked you will be presented with a screen asking for a password. If you have xscreensaver installed you will see its window. Systems without the screensaver will present the LightDM login screen. Entering the password will return you to the system as you left it. Both Xscreensaver and LightDm / Light Locker have the option to log in as a different user.

<a name="xfce-specific-configuration"></a>
### Xfce Specific Configuration

<a name="xfce-power-manager"></a>
#### Xfce Power Manager
When Light Locker is installed Xfce's Power Manager settings gains an additional "Security" tab which allows you to configure Light-locker. Not that much needs configuring. There are options to set how Light Locker works with the screensaver and an option to "Lock screen when system is going for sleep". This is a useful option for laptop when used in conjunction with the option to put the laptop to sleep simply by closing the lid which is found on the General tab in the Xfce Power Manager settings. 
Note this only affects Suspend and Hibernate. Xflock4 (see next section) will still function whatever option is set here.

<a name="xfce-xflock4-and-whisker-menu"></a>
#### Xfce Xflock4 and Whisker Menu
The Whisker menu has a Lock Screen icon. This icon is a shortcut to the Xflock4 command. Both these will stop working when Xscreensaver is removed. To use xflock4 with LightLocker run the following command as user, `xfconf-query -c xfce4-session -p /general/LockCommand -s "dm-tool lock" --create -t string`. Both the icon and the xflock4 keyboard shortcut (Ctrl + Alt + Del) will now lock the session. 
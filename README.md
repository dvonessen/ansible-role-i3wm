i3wm Windows Manager
=========

This role installs and configures i3wm and its dependencies. 


Role Variables
--------------

This role has severall variables to specify the install behavior.

```
i3wm_i3wm_packages:
  - i3-wm
  - libglvnd
  - dmenu
```
You can override this variable to specifiy other packages to install, If you do this you have to add i3wm as well to this variable.

`i3wm_statusbar_package: i3status`
This installs the status bar tool to provide information about your system and calls the JSON API of i3bar

`i3wm_diplay_locker_package: i3lock`
The lock manager. defaults to i3lock

`i3wm_additional_packages`
Here you can add packages as a list, if you wand to install more packages dependent on your system and window manager. e.g: i3blocks, acpi etc.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: thielking.i3wm, i3wm_additional_packages: acpi }

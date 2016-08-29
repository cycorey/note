http://www.hanselman.com/blog/SwitchEasilyBetweenVirtualBoxAndHyperVWithABCDEditBootEntryInWindows81.aspx

Some sites say to use Add/Remove Features to turn the Hyper-V support off, but that seems like a big deal to do what should be a small thing.

Instead, from an administrative command prompt I made a copy of my boot menu with a "No Hyper-V" entry:

Note the first command gives you a GUID and you then copy it and use it with the second command.
```
C:\>bcdedit /copy {current} /d "No Hyper-V" 
The entry was successfully copied to {ff-23-113-824e-5c5144ea}. 

C:\>bcdedit /set {ff-23-113-824e-5c5144ea} hypervisorlaunchtype off 
The operation completed successfully. 
```
Now, this is important. In Windows 8.x, Windows is optimized to startup FAST. And it does. On my Lenovo it starts in about 3 seconds, faster than I can press any buttons to interrupt it. But when I want to dual boot, I need it to really shut down and give me an option to chose this new boot menu.

In order to access the new boot menu, I select Settings (Windows Key + C) then Power, and Restart but hold down shift on the keyboard while clicking Restart with the mouse.

HOLD SHIFT while pressing Restart

You will get this scary looking Blue Screen. Select "Other Operating Systems" and your "No Hyper-V" option is in there.

Windows 8.1 Boot Menu

Selecting No Hyper-V

Now, you can run Virtual Box nicely but still choose Hyper-V when you want. You can confirm VirtualBox works by noting that the Acceleration tab will not be grayed out under System Settings for your VMs. Reboot normally and Hyper-V will be back and ready to go. Here's Android running in VirtualBox via GenyMotion.

Android in an x86 VM in GenyMotion under Virtual Box - Used for Xamarin and Visual Studio Android Development in C#

There's touch support too! If you're not doing Android development like this with Visual Studio and Xamarin, frankly, you're missing out.

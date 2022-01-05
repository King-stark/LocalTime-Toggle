Fix time sync between Windows and macOS. This is native script to fix sync time between Window and Mac OSX when you setup multiboot.
This repository are base on instruction of [harmc0re] (http://www.insanelymac.com/forum/topic/264769-fix-the-time-difference-between-osx86-and-windows-in-multiboot-setups) insanelymac


####Install
1. Download [fix_time_osx.sh](https://raw.githubusercontent.com/hieplpvip/LocalTime-Toggle/master/fix_time_osx.sh).
2. Go to Downloads folder
3. Run command:
```
sudo chmod +x fix_time_osx.sh
./fix_time_osx.sh
```

If all went well, upon pressing enter on that last command, you should notice the time changed again.
Sync the clock with the internet, or manually correct the time, and you're done!

***If you don’t have a relative network environment, please refer to the local way made by [milaoshu1020](https://gitee.com/milaoshu1020/LocalTime-Toggle), or use the way under windows***

### Windows
```
Reg add HKLM\SYSTEM\CurrentControlSet\Control\TimeZoneInformation /v RealTimeIsUniversal /t REG_DWORD /d 1
```
Log in to macos synchronization time completed.

### Macos
```
sudo sh -c "$(curl -kfsSL https://raw.githubusercontent.com/King-stark/LocalTime-Toggle/master/fix_time_osx.sh)"
```
Synchronization time completed.

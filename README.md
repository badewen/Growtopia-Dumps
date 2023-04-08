# Growtopia-Dumps
Growtopia can be dumped with kernel mode dumper.

# How to dump 
There are 2 methods for dumping <br><br>
   <b> First method (easiest) </b>
   - run [KsDumper11](https://github.com/mastercodeon314/KsDumper-11)
   - profit <br><br>
   
   <b> Second method (last resort) </b>
   - use [EfiGuard](https://github.com/Mattiwatti/EfiGuard) to disable the DSE (further details is in the EfiGuard repos)
   - copy KsDumperDriver.sys from [KsDumper](https://github.com/EquiFox/KsDumper) to C:\Windows\System32\drivers
   - run the command `sc create KsDumper binPath= %systemroot%\system32\drivers\KsDumperDriver.sys type= kernel` to install the driver (or service)
   - run this command to start the driver (service? dumper?) `sc start KsDumper`
   - profit

# Limitations
- cant be run (well, you are going to use this for static code analysis dont you?)

# Credits
https://github.com/Mattiwatti/EfiGuard <br>
https://github.com/EquiFox/KsDumper <br>
https://github.com/mastercodeon314/KsDumper-11 <br>
https://github.com/mrexodia/TitanHide 

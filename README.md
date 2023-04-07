# Growtopia-Dumps
Growtopia can be dumped with kernel mode dumper.

# How to dump
 - use [EfiGuard](https://github.com/Mattiwatti/EfiGuard) to disable the DSE (further details is in the EfiGuard repos)
 - copy KsDumperDriver.sys from [KsDumper](https://github.com/EquiFox/KsDumper) to C:\Windows\System32\drivers
 - run the command `sc create KsDumper binPath= %systemroot%\system32\drivers\KsDumperDriver.sys type= kernel` to install the driver (or service)
 - run this command to start the driver (service? dumper?) `sc start KsDumper`
 - profit

# Credits
https://github.com/Mattiwatti/EfiGuard for the dse disabler <br>
https://github.com/EquiFox/KsDumper for the kernel mode dumper

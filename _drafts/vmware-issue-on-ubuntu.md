
The official response from VMWare is to disable Secure Boot from UEFI
https://kb.vmware.com/selfservice/microsites/search.do?language=en_US&cmd=displayKC&externalId=2103112
this is a crap solution considering the point of secure boot is to make things more secure !

I hit a similar issue while trying to install VirtualBox (another desktop based virtualisation product). I quickly made the link between that issue and the one I was having with VMWare and was able to come up with a solution based on forum posts from Gorka.

kernel modules affected are : vmmon vmnet

https://forums.virtualbox.org/viewtopic.php?f=7&t=77363&start=15

Thanks to gorka.eguileor.com/vbox-vmware-in-secureboot-linux



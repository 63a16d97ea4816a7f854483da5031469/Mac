#Mac OS X 10.10.3 running out of disk space after sleep / Potential memory leak?

####5 Ways To Free Up Disk Space on Your OS X Mac
	http://www.howtogeek.com/184091/5-ways-to-free-up-disk-space-on-a-mac/


	http://apple.stackexchange.com/questions/195967/mac-os-x-10-10-3-running-out-of-disk-space-after-sleep-potential-memory-leak

You can check the size of the sleepimage by typing ls -lh /private/var/vm/sleepimage in the Terminal. You can also delete it at any time with sudo rm /private/var/vm/sleepimage as your Mac will just recreate it as needed.


You can check the amount and size of swapfiles on your Macbook with ls -lh /private/var/vm/ in a Terminal window. Note that they are in the same place as the sleepimage, but you can't delete them. If you reboot your Macbook it should clear them up itself.
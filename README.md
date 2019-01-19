# Hackday-Albania-CTF-from-Vulnhub
### About Vulhub.com:
* We all learn in different ways: in a group, by yourself, reading books, watching/listening to other people, making notes or things out   for yourself. 
* Learning the basics & understanding them is essential; this knowledge can be enforced by then putting it into practice. 
  Over the years people have been creating these resources and a lot of time has been put into them, creating ''hidden gems' of training   material. However, unless you know of them, its hard to discover them. 
* So VulnHub was born to cover as many as possible, creating a catalogue of 'stuff' that is (legally) 'breakable, hackable &         exploitable' - allowing you to learn in a safe environment and practise 'stuff' out. 
* In vulhub you can practice your hacking skills through CTF (CAPTURE THE FLAG: contest is a special kind of cybersecurity competition designed to challenge its participants to solve computer security problems and/or capture and defend computer systems.)

## HackDay Albania's 2016 CTF. 
* it is one of the CTF FROM Vulnhub.com
* The level is beginner to intermediate .
* This challenge is all about cracking ubuntu os and finding the flag, There are different approaches to capture the flag this is the one method among them.

link to Download the virtual box .ova file :[ubuntu os](https://www.vulnhub.com/entry/hackday-albania,167/)
## I suggest you to try yourself and then see this approach.

## After downloading the .ova file follow the below steps to capture the Flag:

1. Open virtual box, top left corner click on -->File --> import as shown below

![](https://github.com/vijay-maripi/Hackday-Albania/blob/master/img/1.png)

2. search .ova file from your Downloads

![](https://github.com/vijay-maripi/Hackday-Albania/blob/master/img/2.png)

3. click on import after searching, it will take some time for importing.

![](https://github.com/vijay-maripi/Hackday-Albania/blob/master/img/4.png)

4. now start your ubuntu which is named as Detection Test

![](https://github.com/vijay-maripi/Hackday-Albania/blob/master/img/6.png)

5. after opening ubuntu you will get this screen as shown below, To Capture the flag you need to know "username" & "password"

![](https://github.com/vijay-maripi/Hackday-Albania/blob/master/img/11.png)

6. So to Crack username and password restart your virtual ubuntu 

7. Once you reboot to Grub menu, select the first menu item or the menu item you normally use to boot your Ubuntu system and press e to edit:

![](https://github.com/vijay-maripi/Hackday-Albania/blob/master/img/12.png)

8. Once in the Grub's boot menu edit mode use navigation arrows to locate a line starting with linux and edit it to include read-write mode rw and init=/bin/bash. For example
go to the line starting with linux  and then change as shown below 

FROM:

linux     /boot/vmlinuz-4-4.0-22-generic root=UUID=43ad24d3-e\
c5b-44ee-a099-a88eb9520989 ro  quiet splash $vt_handoff

change to:

linux     /boot/vmlinuz-4-4.0-22-generic root=UUID=43ad24d3-e\
c5b-44ee-a099-a88eb9520989 rw init=/bin/bash

9. Once ready press CTRL+x or F10 to boot.
10. If all went well you should now see root shell command line and your root partition should be mounted with read/write flags. To confirm run:

root@(none):/# mount | grep -w /

![](https://github.com/vijay-maripi/Hackday-Albania/blob/master/img/15.png)

11. Now we are ready to reset root's password. To do so, simply run passwd command with no arguments. When prompted enter your new root password:

root@(none):/# passwd

![](https://github.com/vijay-maripi/Hackday-Albania/blob/master/img/16.png)

All done. Your root's password is now reset.

12. Reboot your system using the following linux command:

root@(none):/# exec /sbin/init

![](https://github.com/vijay-maripi/Hackday-Albania/blob/master/img/17.png)

now press enter and then wait until login screen appears.

13. after that use username: root and password is what you kept.

![](https://github.com/vijay-maripi/Hackday-Albania/blob/master/img/19.png)

14. yeah! now we are in. now what, we should find the flag. Don't worry just use command ls to list the file then you will find something special.

![](https://github.com/vijay-maripi/Hackday-Albania/blob/master/img/20.png)

15. There is text a file named flag.txt. I think this is our flag so lets see what's there inside the file.

use command:

root@hackday:cat flag.txt

![](https://github.com/vijay-maripi/Hackday-Albania/blob/master/img/22.png)

yo atlast we captured the flag. Happy Hacking






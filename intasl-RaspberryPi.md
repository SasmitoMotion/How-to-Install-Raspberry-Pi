# How-to-Install-Raspberry-Pi
This tutorial how to install your Raspberry Pi

First you must to download software in this web : "Raspbian"
    
    https://www.raspberrypi.org/downloads/

copy to sd card "raspbian-wheezy"

and then you must read the blogger how to :

    https://www.raspberrypi.org/documentation/installation/installing-images/windows.md
    https://www.howtoforge.com/tutorial/howto-install-raspbian-on-raspberry-pi/

download win32DiskImager in here :

    http://sourceforge.net/projects/win32diskimager/?source=typ_redirect
    
write your file on sd card "raspbian-wheezy" with win32diskimager

when your write the file, check "commandline" : this example list file in my command line

    dwc_otg.lpm_enable=0 console=ttyAMA0,115200 console=tty1 root=/dev/mmcblk0p2 rootfstype=ext4 elevator=deadline rootwait
 ip=192.168.0.5::192.168.0.1
 
 why the command line has ip in this command, because if you connect on your raspberry pi must need ip address
 
 put your sd card to move on your raspberry pi, connect with cabel ethernet or cable LAN dont forget your charger
 
 setting on your control panel network and sharing center. click "Ethernet" properties choose "IPV4" , example:
 IP Address   : 192.168.0.4
 Subnnet Mask : 255.255.255.0
 
 this ip local address on your pc, and then you can check in command line "ipconfig"
 if your'e done with setting your ip on control panel then you must download dhcpsrv2.5.1.zip, this file location :
 
    http://www.dhcpserver.de/cms/download/
    
  and this tutorial how to running the dhcpserver, dont forget you will must extract this file with winrar
  
    http://www.dhcpserver.de/cms/running_the_server/
  
 in step 1 just click next
 
 in step 2 choose your ip local address ex : 192.168.0.4 and then click next
 
 in step 3 just click next
 
 in step 4 you must create the ip pool between your ip pc and raspberry pi
    ex ip pool : 192.168.0.5-10
 and then click next
 
 in step 5 you must check the "Overwrite existing file" and then click "Write INI File"
 
 in step 6 you must to configure dhcpsrv, (must) " service status : installed " firewall exceptions " configure ", if your status not configured just click "Admin" and then "Firewall exceptions" click "configure" click exit if the status  firewall exceptions "configure" click Finish then enter
 wait a moment because dhcpsvr is to long give your ip address on your raspberry pi
 
 this web to download putty :
 
    http://www.putty.org/
    
 ahaa if you have a stress when you install raspberry pi you must drink tea or coffee. LOL
 
 Putty Configuration : this i get the ip address from dhcpsvr (example)
 
    192.168.0.5     Port : 22
    click SSH     X11 : check X11 forwarding "Enable X11 Forwarding"
    save this file and then open
    

# IBusCommuicatoRR Plugin for RideRunner

IBusCommunicatoRR (pt2) [Update Nov29 2015] / BMW IBus 
11-19-2013, 11:57 AM
Hi People

I was in contact with JanneH0. And we decided that i will continue the Development of his great I-Bus Plugin.
Why new Thread? Because it's difficult to add changes in his Thread. So i started an own. I tested the new Version in my Car 5er E39 with IKE High and 16:9 MK4 Navigation.

The old Thread is here: mp3car forum is down :(

Please tell me, when you have trouble with the new Version.

My adds since Version Dec17 2011:
Oct 29 2013 Update
Added setting to ini file: load/save obc values, 
Added setting to show/hide units of obc values
Added IbusCommunicatoRR.log to log some Strings
Updated IbusCommunicatoRR;sendtoibus (now it works without Checksum)
Updated increased the Ibus IDs up to 300
Updated ReplyMsgID function
Updated ReadMe.txt
Updated Text Scrolling function
Updated Sample Skin

Added new Variables: 
$IBusCommunicatoRR_ARRIVAL$ 
$IBusCommunicatoRR_LIMIT$ 
$IBusCommunicatoRR_OBCTIMER1$
$IBusCommunicatoRR_OBCTIMER2$
$IBusCommunicatoRR_STOPWATCH$
$IBusCommunicatoRR_IBUSCLOCK$
$IBusCommunicatoRR_IBUSDATE$
$IBusCommunicatoRR_NETWORK$
$IBusCommunicatoRR_LANG$
$IBusCommunicatoRR_DISTUNIT$
$IBusCommunicatoRR_SPDUNIT$
$IBusCommunicatoRR_TEMPUNIT$
$IBusCommunicatoRR_CLKFM$
$IBusCommunicatoRR_CNSUNIT$
$IBusCommunicatoRR_MOTOR$

Added new CMDs to 
-Set Distance 
-Set Speedlimit
-Set Timer 1 or 2
-Call a Phonenumber 
-OBC Request
-Set OBC IKE Units/Formats

Added new INDs:
!IbusCommunicatoRR_LIMIT
!IBusCommunicatoRR_MEMO
!IBusCommunicatoRR_AUXHEAT
!IBusCommunicatoRR_TIMER1
!IBusCommunicatoRR_TIMER2

Nov20 2013 Update 
Added CMDs when you turn your Key
IBUSCOMMUNICATORR_IGN_OFF
IBUSCOMMUNICATORR_IGN_ACC
IBUSCOMMUNICATORR_IGN_ON
IBUSCOMMUNICATORR_IGN_START
Added CMD IbusCommunicatoRR;PDCSCROFF : Stops the PDC and exit the pdc.skin

Added PDC stops and exit the pdc.skin if you drive faster than 30km/h or 18mph
Updated ReadMe.txt

Nov23 2013 Update
fixed some Bugs
updated Sample Skin
Updated ReadMe.txt

Nov25 2013 Update
added/updated real AUX Heat Indicator
!IBusCommunicatoRR_AUXVENT:B : State of AUX Ventilation LED (BLINK / OFF)
!IBusCommunicatoRR_AUXHEAT:B : State of AUX Heating LED (BLINK / OFF)

Dec24 2013 Update
added new CMD to tune a frequenz directly on radio: ex. IbusCommunicatoRR;FM;96,3
added new errorscreen when exist a com-port error on RR start
updated ReadMe.txt
updated un-/register.cmd for all windows ( XP --> 8 )

Dec30 2013 Update
bugfix about the ignition commands

Apr26 2014 Update
few changes on sample skin

Jun01 2014 Update
small changes in Text Scrolling Function. IKE Textbar switches back after a moment to ike msg when scrolling was stopped.

Jul03 2014 Update V2.0
New Version 2.0 works with RR Version Jul01_2014

added function by fastforward and -backward for IKE Display if enabled (shows Tracktime on Display)
new function to import Contacts (Name, Numbers and Photo) from VCard. i simple exported my Android S3 mini Contacts as *.vcf file.
optimized the IBUSCOMMUNICATORR;CALL command
updated Sample Skin (BMW Phone, Active Call Popup, Add Contact)
updated ReadMe.txt
tried to add all of them to an installer, but needs some time for installer release  

new CMDs:
IBUSCOMMUNICATORR;BMWPHONE (loads the BMW Phone skin and adds the Contacts from VCard to List) 
IBUSCOMMUNICATORR;ADDCONTACT; (adds new Contact to VCard)
IBUSCOMMUNICATORR;REMOVECONTACT; (deletes Contact from VCard)

new VARs:
$IBUSCOMMUNICATORR_VCARD_NAME$ 
$IBUSCOMMUNICATORR_VCARD_NUMBER$ 
$IBUSCOMMUNICATORR_VCARD_IMG$

new INDs:
!IBUSCOMMUNICATORR_PHONE_GREEN
!IBUSCOMMUNICATORR_PHONE_YELLOW
!IBUSCOMMUNICATORR_PHONE_RED
!IBUSCOMMUNICATORR_PHONE_BTN 

Jul08 2014 Update
Installer is ready for Release

Oct11 2014 Update/Teststate
Integrated RearCam(Webcam) Feature works only with UVC Devices
add this to plugin ini-file. The Installer don't overwrite an existing ini file.:
Code:
; Enable RearCam Integration, True or False (default False)
RearCam=True
add this to your pdc.skin file:
Code:
[ RearCam Area ]
AX,200,140,400,300
for Test you can use this command to enable/disable:
IBUSCOMMUNICATORR;REARCAM

There is a new RearCamFull.skin file. If you click the video screen, you can switch between full or normal view.

For connecting my Rearcam on PC i found a usb uvc video grabber on ebay. itemnumber: 310916545175

Also i did some changes on Phone popup skin.
But the Phone Keys don't work at the moment.

Now the Songpos on seeking is only shown in Radiomode Aux.

Some time left, nobody told me about problems with the RearCam(Webcam) version. that's why i delete the older version in this thread.

Nov08 2014 small Update
added Flash Gauges for ï¿½F, mph and rpm for Diesel on second post of this thread

Dec14 2014 Update
updated doing with Ignition Commands
added a new indicator
!IBUSCOMMUNICATORR_IGN

Dec19 2014 Update
fixed some bugs
optimized OBC Request

Jan27 2015 Update
fixed some bugs
updated Carwings Sample Skin
added Elite 2 Sample Skin ( big thanx to robsbmwerks )

Jan29 2015 Update
added Config Tool for ini file

Apr03 2015 Update
fixed some Bugs
updated SampleSkin, The Radio Screen is only Beta state.
updated ReadMe, Check for some new Commands/Vars/Indicators.
updated Config Tool
added new Flashgauge for Fuel level
Simplistique Skin prepared for IBusCommunicatoRR is placed in 2nd post.
edit:
Fuel Level has a mistake

May03 2015 Update
i think i have fixed the fuel level issue
now there is a new debug mode
replace the existing debug settings with this in your ini file:
Code:
;Debug Level for different Debug Modes (default 1) [0 = off, 1 = low, 2 = mid, 3 = high]
DebugLevel=0
Oct01 2015 Update
updated pdc handling
updated IBusCommunicatoRRConfigTool; you should delete your existing ini file(don't forget backup) and run the config tool.

new CMDs:
IBUSCOMMUNICATORR_DOORS_OPENED
IBUSCOMMUNICATORR_DOORS_CLOSED

new INDs:
!IBusCommunicatoRR_DRV_F_DOOR
!IBusCommunicatoRR_DRV_R_DOOR
!IBusCommunicatoRR_PSG_F_DOOR
!IBusCommunicatoRR_PSG_R_DOOR
!IBusCommunicatoRR_DRV_F_WDW
!IBusCommunicatoRR_DRV_R_WDW
!IBusCommunicatoRR_PSG_F_WDW
!IBusCommunicatoRR_PSG_R_WDW
!IBusCommunicatoRR_TRUNK
!IBusCommunicatoRR_BONNET
!IBusCommunicatoRR_CTR_LOCK

Oct15 2015 Update
small bugfix

Nov29 2015 Update
new RemoteControl CMDs:
IBUSCOMMUNICATORR_RC_LOCK_PRES
IBUSCOMMUNICATORR_RC_UNLOCK_PRES
IBUSCOMMUNICATORR_RC_BOOT_PRES
IBUSCOMMUNICATORR_RC_REL 

new RemoteControl IND:
!IBusCommunicatoRR_RC_BAT_LOWLVL

Next Steps 
need some tests for skin and commands to use phonebuttons for hotline menus
maybe add CD Status for the other Typ of CD-Changer
Optimize Flash Gauges



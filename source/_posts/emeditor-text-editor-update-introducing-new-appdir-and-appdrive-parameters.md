---
title: "EmEditor Text Editor Update: Introducing New $(AppDir) and $(AppDrive) Parameters"
date: 2024-10-18T17:42:53.996Z
updated: 2024-10-22T19:40:16.381Z
tags:
  - product
categories:
  - emeditor
thumbnail: https://thmb.techidaily.com/91f7f58741561326931ca324590beadc475f32b45bcc3a270b10ca0d40e00353.jpg
---

## EmEditor Text Editor Update: Introducing New $(AppDir) and $(AppDrive) Parameters

April 19, 2013 at 6:22 am [#10960](https://tools.techidaily.com/emeditor/products/) 

[![](https://secure.gravatar.com/avatar/f29c043a3cc5c5dac8db4e62939893e9?s=80&d=identicon&r=g)Stefan](https://www.emeditor.com/forums/users/Stefan/ "View Stefan's profile")

Participant

> Posted on: 4/17/2013 1:12 am  
> EmEditor Professional v13 beta (12.9.0) released!
> 
> $(AppDir), $(AppDrive), and $(Clipboard) parameters   
> were added to the External Tool Properties.

 Thank you Yutaka.

 Tested an it works as indented.

 Any change the ${} equivalent form   
 will be added to the Snippets Plugin too?

 – – –

 Examples for $(AppDir)and $(AppDrive) on Tools:

 – having EmEditor on an Thump-Drive:  
 U:SB-DriveEmEditor  
 – having an compiler or interpreter there too:  
 U:SB-DriveWork  
 – you want to call that tool from within EmEditor  
 but the drive letter of the USB drive changes on every PC  
 so you can’t just point to U: always?

 One way is to use this new parameter $(AppDrive)  
 which points to the current drive letter EmEditor is started from:  
 $(AppDrive):SB-DriveWork

 If you have your tool in an sub folder of the EmEditor folder  
 and you don’t want to work with relative paths because that  
 always confuse you, you may want to use the new parameter  
 $(AppDir) which point to the folder EmEditor is started from:  
 ?:SB-DriveEmEditor

 .

<ins class="adsbygoogle"
     style="display:block"
     data-ad-format="autorelaxed"
     data-ad-client="ca-pub-7571918770474297"
     data-ad-slot="1223367746"></ins>

<ins class="adsbygoogle"
     style="display:block"
     data-ad-client="ca-pub-7571918770474297"
     data-ad-slot="8358498916"
     data-ad-format="auto"
     data-full-width-responsive="true"></ins>

<span class="atpl-alsoreadstyle">Also read:</span>
<div><ul>
<li><a href="https://youtube-data.techidaily.com/igh-quality-freely-accessible-music-websites-listed-here-for-2024/"><u>[New] High-Quality, Freely Accessible Music Websites Listed Here for 2024</u></a></li>
<li><a href="https://screen-capture.techidaily.com/updated-2024-approved-action-archetypes-choosing-the-best-7-first-person-shooters/"><u>[Updated] 2024 Approved Action Archetypes Choosing the Best 7 First-Person Shooters</u></a></li>
<li><a href="https://fox-links.techidaily.com/updated-your-ultimate-guide-to-choosing-vr-headsets-opt-for-easy-steps-with-mobile-or-connected-devices-for-2024/"><u>[Updated] Your Ultimate Guide to Choosing VR Headsets Opt for Easy Steps with Mobile or Connected Devices for 2024</u></a></li>
<li><a href="https://extra-support.techidaily.com/2024-approved-level-up-your-playtime-examining-kinemaster-on-android/"><u>2024 Approved Level Up Your Playtime Examining KineMaster on Android</u></a></li>
<li><a href="https://screen-sharing-recording.techidaily.com/2024-approved-secure-and-sync-your-cinematic-recordings-across-platforms/"><u>2024 Approved Secure and Sync Your Cinematic Recordings Across Platforms</u></a></li>
<li><a href="https://win-marvelous.techidaily.com/3windowschk/"><u>3個高效解決辦法：如何將Windows電腦中遭忘記的CHK檔案重新恢復</u></a></li>
<li><a href="https://driver-install.techidaily.com/audio-support-revolution-conexant-hd-driver-for-win11/"><u>Audio Support Revolution: Conexant HD Driver for Win11</u></a></li>
<li><a href="https://youtube-videos.techidaily.com/navigating-the-new-era-youtubes-shorts-fund-explained/"><u>Navigating the New Era YouTube's Shorts Fund Explained</u></a></li>
<li><a href="https://win-marvelous.techidaily.com/tesla-model-s-sound-system-repair-fixing-non-functional-music-features/"><u>Tesla Model S Sound System Repair: Fixing Non-Functional Music Features</u></a></li>
<li><a href="https://win-marvelous.techidaily.com/troubleshooting-guide-fixing-unrecognized-external-hdd-on-ps4/"><u>Troubleshooting Guide: Fixing Unrecognized External HDD on PS4</u></a></li>
<li><a href="https://win-marvelous.techidaily.com/ultimate-guide-starting-up-with-external-media-lenovo-pcs-and-windows-11/"><u>Ultimate Guide: Starting Up With External Media - Lenovo PCs & Windows 11</u></a></li>
<li><a href="https://tech-haven.techidaily.com/unlock-enhanced-developer-capabilities-with-apples-newest-free-ai-powered-software-upgrade/"><u>Unlock Enhanced Developer Capabilities with Apple's Newest Free AI-Powered Software Upgrade</u></a></li>
</ul></div>

<!-- affiliate ads begin -->
<a href="https://aligracehair.sjv.io/c/5597632/1918666/19272" target="_top" id="1918666">
  <img src="//a.impactradius-go.com/display-ad/19272-1918666" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://aligracehair.sjv.io/i/5597632/1918666/19272" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->


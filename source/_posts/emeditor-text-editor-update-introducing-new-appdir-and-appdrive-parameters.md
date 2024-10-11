---
title: "EmEditor Text Editor Update: Introducing New $(AppDir) and $(AppDrive) Parameters"
date: 2024-10-05T16:41:36.344Z
updated: 2024-10-11T16:21:20.781Z
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
<li><a href="https://instagram-videos.techidaily.com/new-in-2024-amp-up-your-ig-videos-crafting-winning-marketing-tactics/"><u>[New] In 2024, Amp Up Your IG Videos Crafting Winning Marketing Tactics</u></a></li>
<li><a href="https://screen-video-capture.techidaily.com/new-in-2024-how-to-use-io-screen-recorder/"><u>[New] In 2024, How to Use IO Screen Recorder</u></a></li>
<li><a href="https://facebook-video-share.techidaily.com/updated-mp3-mastery-guide-top-10-video-to-audio-picks/"><u>[Updated] MP3 Mastery Guide Top 10 Video-to-Audio Picks</u></a></li>
<li><a href="https://screen-mirroring-recording.techidaily.com/updated-professional-analysis-full-potential-of-screenflow-for-mac/"><u>[Updated] Professional Analysis Full Potential of ScreenFlow for Mac</u></a></li>
<li><a href="https://windows11.techidaily.com/converting-your-notepad-to-nighttime-mode-with-ease-on-windows-11/"><u>Converting Your Notepad to Nighttime Mode with Ease on Windows 11</u></a></li>
<li><a href="https://win-marvelous.techidaily.com/fixing-cannot-download-https-videos-effective-strategies-and-tips-for-smooth-playback/"><u>Fixing 'Cannot Download HTTPS Videos': Effective Strategies and Tips for Smooth Playback</u></a></li>
<li><a href="https://win-marvelous.techidaily.com/fixing-linuxacademy-downloads-on-mac-and-windows-step-by-step-troubleshooting-guide/"><u>Fixing Linuxacademy Downloads on Mac & Windows: Step-by-Step Troubleshooting Guide</u></a></li>
<li><a href="https://win-marvelous.techidaily.com/get-premium-naughty-machinima-series-downloaded-as-mp4movaviflvwmv-files/"><u>Get Premium Naughty Machinima Series Downloaded as MP4/MOV/AVI/FLV/WMV Files</u></a></li>
<li><a href="https://win-marvelous.techidaily.com/gomovies-premium-downloads-high-quality-mp4-mov-and-more-for-your-collection/"><u>GoMovies Premium Downloads: High-Quality MP4, MOV & More for Your Collection</u></a></li>
<li><a href="https://location-social.techidaily.com/how-to-fake-snapchat-location-without-jailbreak-on-oppo-find-x7-ultra-drfone-by-drfone-virtual-android/"><u>How to Fake Snapchat Location without Jailbreak On Oppo Find X7 Ultra | Dr.fone</u></a></li>
<li><a href="https://win-marvelous.techidaily.com/how-to-safely-acquire-and-convert-the-movie-dangal-into-various-hd-quality-formats-for-streaming-or-offline-viewing/"><u>How to Safely Acquire and Convert the Movie 'Dangal' Into Various HD Quality Formats for Streaming or Offline Viewing</u></a></li>
<li><a href="https://techtrends.techidaily.com/streamline-your-iphone-with-18-ingenious-shortcuts-app-solutions/"><u>Streamline Your iPhone with 18 Ingenious Shortcuts App Solutions</u></a></li>
</ul></div>

<!-- affiliate ads begin -->
<a href="https://aligracehair.sjv.io/c/5597632/1934288/19272" target="_top" id="1934288">
  <img src="//a.impactradius-go.com/display-ad/19272-1934288" border="0" alt="https://techidaily.com" width="300" height="90"/>
</a>
<img height="0" width="0" src="https://aligracehair.sjv.io/i/5597632/1934288/19272" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->


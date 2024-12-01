---
title: "EmEditor Text Editor Update: Introducing New $(AppDir) and $(AppDrive) Parameters"
date: 2024-11-24T04:37:38.617Z
updated: 2024-11-30T22:10:02.531Z
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
<li><a href="https://youtube-help.techidaily.com/new-pixels-to-perfection-design-tips-for-captivating-banners/"><u>[New] Pixels to Perfection Design Tips for Captivating Banners</u></a></li>
<li><a href="https://extra-approaches.techidaily.com/new-quick-catch-up-effective-methods-for-skipping-edgenuity-courses/"><u>[New] Quick Catch-Up Effective Methods for Skipping Edgenuity Courses</u></a></li>
<li><a href="https://win-marvelous.techidaily.com/4-effective-techniques-for-smooth-file-transfers-to-external-drives/"><u>4 Effective Techniques for Smooth File Transfers to External Drives</u></a></li>
<li><a href="https://win-amazing.techidaily.com/boost-your-acer-predator-helios-300s-fps-with-the-latest-display-drivers/"><u>Boost Your Acer Predator Helios 300'S FPS with the Latest Display Drivers</u></a></li>
<li><a href="https://android-pokemon-go.techidaily.com/catchemall-celebrate-national-pokemon-day-with-virtual-location-on-oneplus-nord-3-5g-drfone-by-drfone-virtual-android/"><u>CatchEmAll Celebrate National Pokémon Day with Virtual Location On OnePlus Nord 3 5G | Dr.fone</u></a></li>
<li><a href="https://win-marvelous.techidaily.com/comprehensive-guide-on-retrieving-information-from-a-damaged-samsung-external-hard-drive/"><u>Comprehensive Guide on Retrieving Information From a Damaged Samsung External Hard Drive</u></a></li>
<li><a href="https://some-approaches.techidaily.com/die-erfolgreichsten-blockbuster-des-sommers-201n-tipps-zur-optimalen-download-strategie/"><u>Die Erfolgreichsten Blockbuster Des Sommers 201N - Tipps Zur Optimalen Download-Strategie</u></a></li>
<li><a href="https://win-marvelous.techidaily.com/gegevens-groeperen-vervulling-zoekachter-gratis-ontwikkel-het-naar-standaard-op-windows-10/"><u>Gegevens Groeperen Vervulling Zoekachter - Gratis Ontwikkel Het Naar Standaard Op Windows 10</u></a></li>
<li><a href="https://win-marvelous.techidaily.com/page-cannot-be-found-http-404-error-detected/"><u>Page Cannot Be Found - HTTP 404 Error Detected</u></a></li>
<li><a href="https://win-marvelous.techidaily.com/ultimate-troubleshooting-tips-unsticking-your-whatsapp-a-comprehensive-walkthrough/"><u>Ultimate Troubleshooting Tips: Unsticking Your WhatsApp - A Comprehensive Walkthrough</u></a></li>
<li><a href="https://video-creation-software.techidaily.com/updated-in-2024-extract-audio-from-webm-files-top-10-converter-tools/"><u>Updated In 2024, Extract Audio From WebM Files Top 10 Converter Tools</u></a></li>
</ul></div>

<!-- affiliate ads begin -->
<iframe width="560" height="315" src="https://www.youtube.com/embed/K4lRBnNnd9k?si=5e0MbdOz-fF6Ry_k" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
<!-- affiliate ads end -->


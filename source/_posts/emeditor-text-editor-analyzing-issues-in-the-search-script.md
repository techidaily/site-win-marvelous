---
title: "EmEditor Text Editor: Analyzing Issues in the Search Script"
date: 2024-10-25T21:23:24.648Z
updated: 2024-10-29T05:52:09.945Z
tags:
  - product
categories:
  - emeditor
thumbnail: https://thmb.techidaily.com/5e307eed611f17e095f5d88028b2351fba3d967d59553e6950da1a4414daed51.jpg
---

## EmEditor Text Editor: Analyzing Issues in the Search Script

Viewing 2 posts - 1 through 2 (of 2 total)

* Author  
Posts
* October 26, 2007 at 9:17 am [#4859](https://tools.techidaily.com/emeditor/products/)  
[![](https://secure.gravatar.com/avatar/e4b3430962364a05c69af317cc2183cf?s=80&d=identicon&r=g)QiaoJiao](https://www.emeditor.com/forums/users/QiaoJiao/ "View QiaoJiao's profile")  
Participant  
Please, say what is wrong with that search script:  
 editor.FindInFiles(“xxx”, “C:web\*.txt”, eeOpenDetectUTF8, eeEncodingSystemDefault);  
 It returns error  
Wrong number of arguments or invalid property assignment  
 I can not figer out where mistake is.  
October 27, 2007 at 12:35 am [#4861](https://tools.techidaily.com/emeditor/products/)  
[![](https://secure.gravatar.com/avatar/a0a6377144ed3636f985d87303f65ed2?s=80&d=identicon&r=g)Yutaka Emura](https://www.emeditor.com/forums/users/yemura/ "View Yutaka Emura's profile")  
Keymaster  
You will need the last parameter _strFilesToIgnore_.  
 So the correct code is:  
    
	editor.FindInFiles("xxx", "C:web*.txt", eeOpenDetectUTF8, eeEncodingSystemDefault, "");
* Author  
Posts

Viewing 2 posts - 1 through 2 (of 2 total)

* You must be logged in to reply to this topic.

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
<li><a href="https://instagram-video-files.techidaily.com/new-2024-approved-effortless-method-to-post-sites-on-ig-storyposts/"><u>[New] 2024 Approved Effortless Method to Post Sites on IG Story/Posts</u></a></li>
<li><a href="https://instagram-clips.techidaily.com/new-enhancing-viewer-experience-vertical-videos-in-final-cut-pro-x/"><u>[New] Enhancing Viewer Experience Vertical Videos in Final Cut Pro X</u></a></li>
<li><a href="https://win-marvelous.techidaily.com/windowsmacbookgoogle-chrome/"><u>「關於Windows或MacBook的Google Chrome書籤儲存位置解析」</u></a></li>
<li><a href="https://buynow-info.techidaily.com/breaking-down-overwatch-a-riveting-group-combat-adventure-unveiled/"><u>Breaking Down Overwatch - A Riveting Group Combat Adventure Unveiled!</u></a></li>
<li><a href="https://buynow-help.techidaily.com/bring-the-arena-to-your-living-room-with-nba-2k19-elite-sports-entertainment/"><u>Bring the Arena to Your Living Room With NBA 2K19: Elite Sports Entertainment</u></a></li>
<li><a href="https://win-marvelous.techidaily.com/efektywny-porzadownik-kopii-zapasowych-dla-serwera-windows-jak-ustalic-drugi-tydzien-na-sukces/"><u>Efektywny Porządownik Kopii Zapasowych Dla Serwera Windows: Jak Ustalić Drugi Tydzień Na Sukces</u></a></li>
<li><a href="https://win-marvelous.techidaily.com/effortless-strategies-seamlessly-transitioning-your-whs-201/"><u>Effortless Strategies: Seamlessly Transitioning Your WHS 201</u></a></li>
<li><a href="https://common-error.techidaily.com/error-code-explained-fixing-long-wait-times-for-semaphore-signals-0x80070079/"><u>Error Code Explained: Fixing Long Wait Times for Semaphore Signals (0X80070079)</u></a></li>
<li><a href="https://win-marvelous.techidaily.com/guia-facil-para-respaldo-y-carga-de-archivos-desde-su-pc-hacia-un-almacenamiento-en-la-nube-sin-coste/"><u>Guía Fácil Para Respaldo Y Carga De Archivos Desde Su PC Hacia Un Almacenamiento en La Nube Sin Coste</u></a></li>
<li><a href="https://win-marvelous.techidaily.com/heat-treatment-processes-can-significantly-alter-an-alloys-mechanical-properties/"><u>Heat Treatment Processes Can Significantly Alter an Alloy's Mechanical Properties.</u></a></li>
<li><a href="https://activate-lock.techidaily.com/in-2024-3-effective-ways-to-unlock-icloud-account-without-password-from-iphone-11-pro-by-drfone-ios/"><u>In 2024, 3 Effective Ways to Unlock iCloud Account Without Password From iPhone 11 Pro</u></a></li>
<li><a href="https://easy-unlock-android.techidaily.com/in-2024-unlock-your-realme-12-pro-5g-phone-with-ease-the-3-best-lock-screen-removal-tools-by-drfone-android/"><u>In 2024, Unlock Your Realme 12 Pro 5G Phone with Ease The 3 Best Lock Screen Removal Tools</u></a></li>
<li><a href="https://fake-location.techidaily.com/life360-circle-everything-you-need-to-know-on-itel-p55t-drfone-by-drfone-virtual-android/"><u>Life360 Circle Everything You Need to Know On Itel P55T | Dr.fone</u></a></li>
<li><a href="https://win-marvelous.techidaily.com/removed-startup-partition-say-goodbye-to-windows-7-8-10-and-11/"><u>Removed Startup Partition: Say Goodbye to Windows 7, 8, 10 & 11</u></a></li>
<li><a href="https://windows11.techidaily.com/set-up-a-fast-safe-login-windows-hello-basics/"><u>Set Up a Fast, Safe Login: Windows Hello Basics</u></a></li>
<li><a href="https://win-marvelous.techidaily.com/there-are-various-types-of-scrubbers-wet-dry-semi-dry-electrostatic-each-suitable-for-different-applications/"><u>There Are Various Types of Scrubbers (Wet, Dry, Semi-Dry, Electrostatic), Each Suitable for Different Applications.</u></a></li>
<li><a href="https://win-marvelous.techidaily.com/1728498455515-windows-serverwbadmin/"><u>Windows ServerでWbadminツールを利用した効率的なバックアップ方法</u></a></li>
</ul></div>

<!-- affiliate ads begin -->
<a href="https://appsumo.8odi.net/c/5597632/2037359/7443" target="_top" id="2037359">
  <img src="//a.impactradius-go.com/display-ad/7443-2037359" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://appsumo.8odi.net/i/5597632/2037359/7443" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->


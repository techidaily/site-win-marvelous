---
title: One-at-a-Time Item Searching Technique Using EmEditor for Text Files
date: 2024-10-27T20:13:12.318Z
updated: 2024-11-03T19:04:39.917Z
tags:
  - product
categories:
  - emeditor
thumbnail: https://thmb.techidaily.com/6b70f639163cfe01d6518c08ef2693a5f686b7373d5c47d7a53f258bef450907.jpg
---

## One-at-a-Time Item Searching Technique Using EmEditor for Text Files

Viewing 6 posts - 1 through 6 (of 6 total)

* Author  
Posts
* January 11, 2015 at 10:45 am [#19768](https://tools.techidaily.com/emeditor/products/)  
[![](https://secure.gravatar.com/avatar/da07de1ac7e90cc419eda36ea3e88646?s=80&d=identicon&r=g)Mike Fur](https://www.emeditor.com/forums/users/mike-fur/ "View Mike Fur's profile")  
Participant  
e.g. I’d like to search the numbers in “Column 2” against “Column 1” and output what matches.  
 I noticed that “multiline” function in EmEditor. However, I am not able to search the numbers in “Column 2” one by one but rather as a whole string.  
 Just wondering if anyone has a solution for multiple search? Thanks,  
column 1 column 2  
 1 1  
 5 2  
 8 3  
 10 4  
 25 5  
 29 6  
 31 7  
 8  
 9  
 10  
 11  
 12  
 13  
 14  
 15  
 16  
 17  
 18  
 19  
 20  
 21  
 22  
 23  
 24  
 25  
 26  
 27  
 28  
 29  
 30  
 31  
January 11, 2015 at 3:12 pm [#19769](https://tools.techidaily.com/emeditor/products/)  
[![](https://secure.gravatar.com/avatar/a0a6377144ed3636f985d87303f65ed2?s=80&d=identicon&r=g)Yutaka Emura](https://www.emeditor.com/forums/users/yemura/ "View Yutaka Emura's profile")  
Keymaster  
Hello Mike,  
I am not sure exactly what you want to do. Can you show me an example?  
Thank you!  
January 11, 2015 at 4:45 pm [#19771](https://tools.techidaily.com/emeditor/products/)  
[![](https://secure.gravatar.com/avatar/da07de1ac7e90cc419eda36ea3e88646?s=80&d=identicon&r=g)Mike Fur](https://www.emeditor.com/forums/users/mike-fur/ "View Mike Fur's profile")  
Participant  
Hi Thanks for your instant response!  
 This would be like a search/find function but it automatically search a list of items one by one in another file instead of enter each item manually.  
For instance:  
 1st file:  
 ID1 description  
 1 absent  
 2 present  
 3 present  
 4 absent  
 5 absent  
 6 present  
 7 present  
 8 present  
 9 absent  
 10 present  
 11 present  
 12 present  
 13 present  
 14 absent  
 15 absent  
 16 present  
 17 present  
 18 present  
 19 present  
 20 present  
 21 present  
 22 absent  
 23 absent  
 24 absent  
 25 absent  
 26 absent  
 27 absent  
 28 absent  
 29 absent  
2nd file:  
 ID2  
 1  
 5  
 7  
 3  
 23  
 5  
 24  
 12  
 25  
 2  
 6  
 11  
 18  
 16  
The results:  
 1 absent  
 5 absent  
 7 present  
 3 present  
 23 absent  
 5 absent  
 24 absent  
 12 present  
 25 absent  
 2 present  
 6 present  
 11 present  
 18 present  
 16 present  
January 11, 2015 at 9:10 pm [#19772](https://tools.techidaily.com/emeditor/products/)  
[![](https://secure.gravatar.com/avatar/a0a6377144ed3636f985d87303f65ed2?s=80&d=identicon&r=g)Yutaka Emura](https://www.emeditor.com/forums/users/yemura/ "View Yutaka Emura's profile")  
Keymaster  
Hello Mike,  
Thanks for explanation. This is like the JOINT feature of SQL, and I was thinking about this in future versions. Please wait for future versions.  
Meanwhile, you can write a macro like this:  
```  
doc1 = editor.Documents.Item(1);  
doc2 = editor.Documents.Item(2);  
editor.NewFile();  
doc3 = document;  
doc1.Activate();  
nLines1 = doc1.GetLines();  
doc2.Activate();  
nLines2 = doc2.GetLines();  
for(y2 = 1; y2 <= nLines2; y2++) {  
	doc2.Activate();  
	s2 = doc2.GetLine(y2);  
	if(s2 == "") continue;  
	doc1.Activate();  
	for(y1 = 1; y1 <= nLines1; y1++) {  
		s1 = doc1.GetCell(y1, 1, eeCellIncludeNone);  
		if(s1 == "") continue;  
		if(s1 == s2) {  
			sResult = doc1.GetCell(y1, 2, eeCellIncludeNone);  
			doc3.Activate();  
			doc3.writeln(s2 + "\t" + sResult);  
			break;  

```  
Thanks!  
January 12, 2015 at 7:29 am [#19773](https://tools.techidaily.com/emeditor/products/)  
[![](https://secure.gravatar.com/avatar/da07de1ac7e90cc419eda36ea3e88646?s=80&d=identicon&r=g)Mike Fur](https://www.emeditor.com/forums/users/mike-fur/ "View Mike Fur's profile")  
Participant  
Thanks, Yutaka  
 This would be a very useful function in various areas. Hope to use it in the future versions soon!  
January 21, 2015 at 4:05 pm [#19802](https://tools.techidaily.com/emeditor/products/)  
[![](https://secure.gravatar.com/avatar/a0a6377144ed3636f985d87303f65ed2?s=80&d=identicon&r=g)Yutaka Emura](https://www.emeditor.com/forums/users/yemura/ "View Yutaka Emura's profile")  
Keymaster  
Hello Mike,  
This feature is added now:  
<https://www.emeditor.com/forums/topic/emeditor-v14-8-0-beta-1/>  
Join CSV feature.
* Author  
Posts

Viewing 6 posts - 1 through 6 (of 6 total)

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
<li><a href="https://eaxpv-info.techidaily.com/new-the-8-most-critical-blunders-to-elude-as-a-rookie-youtuber/"><u>[New] The 8 Most Critical Blunders to Elude as a Rookie YouTuber</u></a></li>
<li><a href="https://win-marvelous.techidaily.com/1-effizientes-wissen-um-samsung-ssd-datenubertragung-fertigstellen-von-projekten-erfolgreicher/"><u>1. Effizientes Wissen Um Samsung-SSD Datenübertragung - Fertigstellen Von Projekten Erfolgreicher</u></a></li>
<li><a href="https://android-pokemon-go.techidaily.com/9-mind-blowing-tricks-to-hatch-eggs-in-pokemon-go-without-walking-on-nokia-c12-drfone-by-drfone-virtual-android/"><u>9 Mind-Blowing Tricks to Hatch Eggs in Pokemon Go Without Walking On Nokia C12 | Dr.fone</u></a></li>
<li><a href="https://win-marvelous.techidaily.com/1728486764535-windows-11/"><u>間違い電:Windows 11環境下で失われたファイルを取り戻せるテクニック</u></a></li>
<li><a href="https://win-marvelous.techidaily.com/comparing-das-and-nas-understanding-their-key-distinctions/"><u>Comparing DAS and NAS: Understanding Their Key Distinctions</u></a></li>
<li><a href="https://win-marvelous.techidaily.com/effortless-setup-for-windows-10-directly-on-your-new-solid-state-drive-with-cddvd-or-without/"><u>Effortless Setup for Windows 10 Directly on Your New Solid State Drive: With CD/DVD or Without!</u></a></li>
<li><a href="https://tech-renaissance.techidaily.com/how-to-extend-your-macs-active-hours-and-avoid-unwanted-hibernation/"><u>How to Extend Your Mac's Active Hours & Avoid Unwanted Hibernation</u></a></li>
<li><a href="https://digital-screen-recording.techidaily.com/how-to-master-video-capture-using-adobe-presenter/"><u>How to Master Video Capture Using Adobe Presenter</u></a></li>
<li><a href="https://win-marvelous.techidaily.com/how-to-seamlessly-share-crisp-pictures-from-iphone-with-your-android-phone-a-guide-for-3-techniques/"><u>How to Seamlessly Share Crisp Pictures From iPhone with Your Android Phone: A Guide for 3 Techniques</u></a></li>
<li><a href="https://activate-lock.techidaily.com/in-2024-3-effective-ways-to-unlock-icloud-account-without-password-on-iphone-6s-by-drfone-ios/"><u>In 2024, 3 Effective Ways to Unlock iCloud Account Without Password On iPhone 6s</u></a></li>
<li><a href="https://win-marvelous.techidaily.com/mastering-the-art-of-windows-booting-processes-complete-insights-and-essential-tips/"><u>Mastering the Art of Windows Booting Processes: Complete Insights & Essential Tips</u></a></li>
<li><a href="https://win-blog.techidaily.com/new-tips-for-a-smooth-gameplay-preventing-rocket-league-from-crashing/"><u>New Tips for a Smooth Gameplay: Preventing Rocket League From Crashing</u></a></li>
<li><a href="https://win-marvelous.techidaily.com/quick-and-easy-guide-top-4-methods-for-successful-iphone-copying/"><u>Quick & Easy Guide: Top 4 Methods for Successful iPhone Copying</u></a></li>
<li><a href="https://win-solutions.techidaily.com/starfield-cpu-overload-solutions-top-tips-to-optimize-performance/"><u>Starfield CPU Overload Solutions - Top Tips to Optimize Performance</u></a></li>
<li><a href="https://win-marvelous.techidaily.com/superior-norton-goback-alternatives-for-enhanced-system-restore-functionality-in-windows/"><u>Superior Norton GoBack Alternatives for Enhanced System Restore Functionality in Windows</u></a></li>
<li><a href="https://tech-savvy.techidaily.com/transforming-interaction-with-xr-digital-twins-and-spatial-tech-a-comprehensive-enterprise-handbook-for-enhanced-ux-zdnet-insights/"><u>Transforming Interaction with XR, Digital Twins & Spatial Tech: A Comprehensive Enterprise Handbook for Enhanced UX | ZDNet Insights</u></a></li>
<li><a href="https://hardware-help.techidaily.com/windows-compatible-amd-radeon-hd-6350-driver-download-keeping-your-system-up-to-date/"><u>Windows Compatible AMD Radeon HD 6350 Driver Download: Keeping Your System Up-to-Date</u></a></li>
</ul></div>

<!-- affiliate ads begin -->
<a href="https://aligracehair.sjv.io/c/5597632/2016143/19272" target="_top" id="2016143">
  <img src="//a.impactradius-go.com/display-ad/19272-2016143" border="0" alt="https://techidaily.com" width="300" height="90"/>
</a>
<img height="0" width="0" src="https://aligracehair.sjv.io/i/5597632/2016143/19272" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->


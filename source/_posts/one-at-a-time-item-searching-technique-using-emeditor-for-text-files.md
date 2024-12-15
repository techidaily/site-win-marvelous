---
title: One-at-a-Time Item Searching Technique Using EmEditor for Text Files
date: 2024-12-12T10:08:43.711Z
updated: 2024-12-14T23:26:28.237Z
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
<li><a href="https://facebook-video-footage.techidaily.com/new-essential-list-7-cost-free-video-tags-extractors-on-youtube-for-2024/"><u>[New] Essential List 7 Cost-Free Video Tags Extractors on YouTube for 2024</u></a></li>
<li><a href="https://on-screen-recording.techidaily.com/updated-how-to-archive-video-team-hangouts-effectively-for-2024/"><u>[Updated] How to Archive Video Team Hangouts Effectively for 2024</u></a></li>
<li><a href="https://solve-howtos.techidaily.com/diagnosing-hardware-woes-why-wont-my-system-acknowledge-its-hard-disk-tips-by-yl-software-experts/"><u>Diagnosing Hardware Woes: Why Won't My System Acknowledge Its Hard Disk? - Tips by YL Software Experts</u></a></li>
<li><a href="https://win-marvelous.techidaily.com/effective-methods-for-removing-redundant-programs-and-services-yl-computing-insights/"><u>Effective Methods for Removing Redundant Programs & Services - YL Computing Insights</u></a></li>
<li><a href="https://win-marvelous.techidaily.com/effective-strategies-for-resolving-sound-card-issues-insights-from-yl-computings-latest-guide/"><u>Effective Strategies for Resolving Sound Card Issues: Insights From YL Computing's Latest Guide</u></a></li>
<li><a href="https://tech-renaissance.techidaily.com/expert-advice-restoring-your-surface-pros-ability-to-connect-to-wireless-networks/"><u>Expert Advice: Restoring Your Surface Pro’s Ability to Connect to Wireless Networks</u></a></li>
<li><a href="https://win-marvelous.techidaily.com/high-definition-game-of-thrones-backgrounds-and-wallpapers-by-yl-computing-premium-static-set/"><u>High Definition Game of Thrones Backgrounds & Wallpapers by YL Computing - Premium Static Set</u></a></li>
<li><a href="https://win-blog.techidaily.com/how-to-overcome-the-0xc19001e1-error-on-your-windows-11-system/"><u>How to Overcome the '0Xc19001e1 Error' On Your Windows 11 System</u></a></li>
<li><a href="https://win-marvelous.techidaily.com/identifying-graphic-card-issues-a-guide-expert-tips-by-yl-computing/"><u>Identifying Graphic Card Issues: A Guide - Expert Tips by YL Computing</u></a></li>
<li><a href="https://sim-unlock.techidaily.com/in-2024-how-to-change-your-sim-pin-code-on-your-lava-agni-2-5g-phone-by-drfone-android/"><u>In 2024, How To Change Your SIM PIN Code on Your Lava Agni 2 5G Phone</u></a></li>
<li><a href="https://win-marvelous.techidaily.com/no-sound-troubleshooting-guide-for-windows-users-by-yl-software-experts/"><u>No Sound Troubleshooting Guide for Windows Users by YL Software Experts</u></a></li>
<li><a href="https://win-marvelous.techidaily.com/resolving-strange-noises-in-your-windows-pc-hard-drive-tips-and-tricks-with-yl-software/"><u>Resolving Strange Noises in Your Windows PC Hard Drive: Tips & Tricks with YL Software</u></a></li>
<li><a href="https://extra-skills.techidaily.com/ringtone-revelry-top-choices-for-laugh-inducing-calls-for-2024/"><u>Ringtone Revelry Top Choices for Laugh-Inducing Calls for 2024</u></a></li>
<li><a href="https://win-marvelous.techidaily.com/solving-driver-problems-expert-tips-from-yl-computings-software-suite/"><u>Solving Driver Problems: Expert Tips From YL Computing's Software Suite</u></a></li>
<li><a href="https://fox-that.techidaily.com/track-down-lost-or-stolen-iphones-via-apples-find-my-app/"><u>Track Down Lost or Stolen iPhones via Apple's Find My App</u></a></li>
</ul></div>

<!-- affiliate ads begin -->
<iframe width="560" height="315" src="https://www.youtube.com/embed/U6lCtLUeROA?si=se6OFuis9JpcTGJf" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
<!-- affiliate ads end -->


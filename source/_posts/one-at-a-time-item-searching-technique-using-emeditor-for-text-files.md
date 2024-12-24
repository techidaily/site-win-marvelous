---
title: One-at-a-Time Item Searching Technique Using EmEditor for Text Files
date: 2024-12-21T09:30:14.531Z
updated: 2024-12-23T23:11:50.148Z
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
<li><a href="https://some-knowledge.techidaily.com/new-exemplary-cloud-services-for-biz-needs/"><u>[New] Exemplary Cloud Services for Biz Needs</u></a></li>
<li><a href="https://youtube-webster.techidaily.com/ed-2024-approved-how-to-shave-seconds-off-your-youtube-video-submission/"><u>[Updated] 2024 Approved How to Shave Seconds Off Your YouTube Video Submission</u></a></li>
<li><a href="https://fox-friendly.techidaily.com/updated-exclusive-preview-general-knowledge-quiz-networks-of-2024/"><u>[Updated] Exclusive Preview General Knowledge Quiz Networks of 2024</u></a></li>
<li><a href="https://tiktok-video-recordings.techidaily.com/updated-in-2024-journey-to-crafting-a-unique-alphanumeric-marker-for-tiktok/"><u>[Updated] In 2024, Journey to Crafting a Unique Alphanumeric Marker for TikTok</u></a></li>
<li><a href="https://fox-hovers.techidaily.com/2024-approved-navigating-screen-space-enlargement-on-youtube/"><u>2024 Approved Navigating Screen Space Enlargement on YouTube</u></a></li>
<li><a href="https://win-marvelous.techidaily.com/how-can-you-fix-a-damaged-graphics-card-insights-from-yl-computings-expertise/"><u>How Can You Fix a Damaged Graphics Card? Insights From YL Computing's Expertise</u></a></li>
<li><a href="https://sim-unlock.techidaily.com/how-to-check-if-your-samsung-galaxy-s24-is-unlocked-by-drfone-android/"><u>How To Check if Your Samsung Galaxy S24 Is Unlocked</u></a></li>
<li><a href="https://activate-lock.techidaily.com/in-2024-the-ultimate-guide-to-bypassing-icloud-activation-lock-from-apple-iphone-7-by-drfone-ios/"><u>In 2024, The Ultimate Guide to Bypassing iCloud Activation Lock from Apple iPhone 7</u></a></li>
<li><a href="https://win-marvelous.techidaily.com/is-your-graphics-card-up-to-the-task-diagnosing-hardware-efficiency-with-yl-software-techniques/"><u>Is Your Graphics Card Up to the Task? Diagnosing Hardware Efficiency with YL Software Techniques</u></a></li>
<li><a href="https://win-marvelous.techidaily.com/no-image-on-monitor-discover-why-and-how-to-fix-it-with-yl-software-solutions/"><u>No Image on Monitor? Discover Why and How to Fix It with YL Software Solutions</u></a></li>
<li><a href="https://win-marvelous.techidaily.com/revive-your-scanner-guide-to-updating-drivers-using-yl-software-solutions/"><u>Revive Your Scanner: Guide to Updating Drivers Using YL Software Solutions</u></a></li>
<li><a href="https://win-marvelous.techidaily.com/self-healing-concrete-contains-healing-agents-that-are-activated-when-cracks-form-enabling-automatic-repair-and-extending-structure-life/"><u>Self-Healing Concrete Contains Healing Agents that Are Activated when Cracks Form, Enabling Automatic Repair and Extending Structure Life.</u></a></li>
<li><a href="https://fox-hovers.techidaily.com/the-ultimate-srt-file-craftsmanship-manual-for-2024/"><u>The Ultimate SRT File Craftsmanship Manual for 2024</u></a></li>
<li><a href="https://some-approaches.techidaily.com/transforming-brands-with-language-mastery-techniques-for-2024/"><u>Transforming Brands with Language Mastery Techniques for 2024</u></a></li>
<li><a href="https://win-marvelous.techidaily.com/ultimate-bmw-z4-roadster-hd-backdrops-for-any-device-innovative-designs-from-yl-computings-imagery-studio/"><u>Ultimate BMW Z4 Roadster HD Backdrops for Any Device: Innovative Designs From YL Computing's Imagery Studio</u></a></li>
<li><a href="https://win-marvelous.techidaily.com/unlock-full-potential-guaranteeing-peak-efficiency-for-your-pc-with-yl-computing-and-ys-software-strategies/"><u>Unlock Full Potential: Guaranteeing Peak Efficiency for Your PC with YL Computing & YS Software Strategies</u></a></li>
<li><a href="https://win-marvelous.techidaily.com/yl-software-solutions-for-restarting-malfunctioned-windows-services/"><u>YL Software Solutions for Restarting Malfunctioned Windows Services</u></a></li>
</ul></div>

<!-- affiliate ads begin -->
<iframe width="560" height="315" src="https://www.youtube.com/embed/JMgRzDANfSQ?si=NDy01ntXGGOi1Uxs" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
<!-- affiliate ads end -->


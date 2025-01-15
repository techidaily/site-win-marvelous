---
title: One-at-a-Time Item Searching Technique Using EmEditor for Text Files
date: 2025-01-12T07:12:02.407Z
updated: 2025-01-14T23:42:07.995Z
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
<li><a href="https://digital-screen-recording.techidaily.com/new-in-2024-the-evolutionary-path-from-novice-to-expert-in-audio-recording-for-film/"><u>[New] In 2024, The Evolutionary Path From Novice to Expert in Audio Recording for Film</u></a></li>
<li><a href="https://extra-resources.techidaily.com/updated-boosting-media-throughput-in-microsoft-presentations/"><u>[Updated] Boosting Media Throughput in Microsoft Presentations</u></a></li>
<li><a href="https://youtube-sure.techidaily.com/ed-in-2024-hasty-methods-for-mixed-up-youtube-playback-sequence/"><u>[Updated] In 2024, Hasty Methods for Mixed-Up YouTube Playback Sequence</u></a></li>
<li><a href="https://android-frp.techidaily.com/easy-guide-how-to-bypass-oneplus-ace-2-frp-android-10111213-by-drfone-android/"><u>Easy Guide How To Bypass OnePlus Ace 2 FRP Android 10/11/12/13</u></a></li>
<li><a href="https://win-marvelous.techidaily.com/experience-spooky-atmosphere-with-original-halloween-desktops-images-and-photo-wallpapers-from-yl-software/"><u>Experience Spooky Atmosphere with Original Halloween Desktops Images and Photo Wallpapers From YL Software</u></a></li>
<li><a href="https://win-marvelous.techidaily.com/how-and-why-do-lcd-screens-experience-flickering-issues-understanding-with-yl-computings-technical-analysis/"><u>How and Why Do LCD Screens Experience Flickering Issues? Understanding with YL Computing's Technical Analysis</u></a></li>
<li><a href="https://win-marvelous.techidaily.com/is-your-graphics-card-malfunction-putting-your-pcs-health-at-risk-expert-insight-from-yl-computing/"><u>Is Your Graphics Card Malfunction Putting Your PC's Health at Risk? Expert Insight From YL Computing</u></a></li>
<li><a href="https://win-marvelous.techidaily.com/master-your-system-customizing-power-management-options-with-insights-from-yl-software/"><u>Master Your System: Customizing Power Management Options with Insights From YL Software</u></a></li>
<li><a href="https://win-marvelous.techidaily.com/mastering-window-security-settings-a-detailed-tutorial-on-adjusting-the-firewall-from-control-panel-with-help-from-yl-software-experts/"><u>Mastering Window Security Settings: A Detailed Tutorial on Adjusting the Firewall From Control Panel with Help From YL Software Experts</u></a></li>
<li><a href="https://howto.techidaily.com/oppo-reno-9a-bootloop-problem-how-to-fix-it-without-data-loss-drfone-by-drfone-fix-android-problems-fix-android-problems/"><u>Oppo Reno 9A Bootloop Problem, How to Fix it Without Data Loss | Dr.fone</u></a></li>
<li><a href="https://review-topics.techidaily.com/remove-google-frp-lock-on-motorola-moto-g04-by-drfone-android-unlock-remove-google-frp/"><u>Remove Google FRP lock on Motorola Moto G04</u></a></li>
<li><a href="https://win-howtos.techidaily.com/solved-permanent-lag-on-valorants-launch-screen-steps-for-a-smooth-start/"><u>Solved! Permanent Lag on Valorant's Launch Screen: Steps for a Smooth Start</u></a></li>
<li><a href="https://win-marvelous.techidaily.com/solving-scanning-issues-making-your-printers-display-visible-again-expert-tips-from-yl-computing/"><u>Solving Scanning Issues: Making Your Printer's Display Visible Again - Expert Tips From YL Computing</u></a></li>
<li><a href="https://win-marvelous.techidaily.com/troubleshooting-tips-solving-boot-issues-on-your-pc-yl-software-guide/"><u>Troubleshooting Tips: Solving Boot Issues on Your PC - YL Software Guide</u></a></li>
<li><a href="https://win-forum.techidaily.com/understanding-and-accessing-pc-specifications-in-windows-11-without-third-party-software/"><u>Understanding and Accessing PC Specifications in Windows 11 without Third-Party Software</u></a></li>
<li><a href="https://win-marvelous.techidaily.com/understanding-hard-drive-malfunctions-expert-analysis-by-yl-software-solutions/"><u>Understanding Hard Drive Malfunctions: Expert Analysis by YL Software Solutions</u></a></li>
<li><a href="https://some-guidance.techidaily.com/unlocking-fun-navigating-ifunny-meme-app-for-2024/"><u>Unlocking Fun Navigating iFunny Meme App for 2024</u></a></li>
</ul></div>

<!-- affiliate ads begin -->
<iframe width="560" height="315" src="https://www.youtube.com/embed/omWG4u39lmE?si=yk1AEo_gzDpGjYbl" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
<!-- affiliate ads end -->


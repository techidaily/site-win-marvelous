---
title: One-at-a-Time Item Searching Technique Using EmEditor for Text Files
date: 2025-02-03T22:27:54.278Z
updated: 2025-02-09T03:33:40.167Z
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
<li><a href="https://article-helps.techidaily.com/new-barebones-calm-music-selection-for-2024/"><u>[New] Barebones Calm Music Selection for 2024</u></a></li>
<li><a href="https://fox-http.techidaily.com/updated-2024-approved-distinguished-choices-top-iphone-sound-artisans/"><u>[Updated] 2024 Approved Distinguished Choices Top iPhone Sound Artisans</u></a></li>
<li><a href="https://fox-glue.techidaily.com/updated-in-2024-photographic-precision-against-shake/"><u>[Updated] In 2024, Photographic Precision Against Shake</u></a></li>
<li><a href="https://win-marvelous.techidaily.com/1-schnelles-und-einfaches-sicherstellen-ihrer-daten-mit-wd-mycloud-externe-festplatten-backup-anleitung/"><u>1. Schnelles Und Einfaches Sicherstellen Ihrer Daten Mit WD MyCloud - Externe Festplatten-Backup-Anleitung</u></a></li>
<li><a href="https://youtube-stream.techidaily.com/2024-approved-from-footage-to-fame-premiere-pro-edition-tricks-for-youtube/"><u>2024 Approved From Footage to Fame Premiere Pro Edition Tricks for YouTube</u></a></li>
<li><a href="https://tiktok-videos.techidaily.com/2024-approved-the-template-trick-for-eye-catching-tiktok-creation-mastery/"><u>2024 Approved The Template Trick for Eye-Catching TikTok Creation Mastery</u></a></li>
<li><a href="https://win-marvelous.techidaily.com/disco-de-reposicion-para-servidor-windows-2022-por-creador-z-tecnologia-rapida-y-protegida-mas-fiable/"><u>Disco De Reposición Para Servidor Windows 2022 Por Creador Z: Tecnología Rápida Y Protegida Más Fiable</u></a></li>
<li><a href="https://buynow-reviews.techidaily.com/dive-into-the-world-of-high-end-gaming-with-our-in-depth-review-of-the-stylish-and-powerful-dell-alienware-aurora-r9-pc/"><u>Dive Into the World of High-End Gaming with Our In-Depth Review of the Stylish and Powerful Dell Alienware Aurora R9 PC</u></a></li>
<li><a href="https://win-marvelous.techidaily.com/effective-ways-to-tackle-elevated-disk-consumption-from-antimalware-service-exe/"><u>Effective Ways to Tackle Elevated Disk Consumption From Antimalware Service Exe</u></a></li>
<li><a href="https://win-marvelous.techidaily.com/effortless-and-free-solutions-for-protecting-and-copying-your-xbox-consoles-save-data/"><u>Effortless & Free Solutions for Protecting and Copying Your Xbox Console's Save Data</u></a></li>
<li><a href="https://win-marvelous.techidaily.com/geavanceerde-tips-voor-uitwisseling-van-wechat-geschiedenis-vanaf-android-opschreiden-op-ios/"><u>Geavanceerde Tips Voor Uitwisseling Van WeChat Geschiedenis Vanaf Android Opschreiden Op iOS</u></a></li>
<li><a href="https://extra-tips.techidaily.com/in-depth-analysis-the-powerhouse-that-is-dji-phantom-3/"><u>In-Depth Analysis The Powerhouse That Is DJI Phantom 3</u></a></li>
<li><a href="https://win-marvelous.techidaily.com/maximiser-les-capacites-de-copie-robotique-sous-windows-11-guide-et-meilleurs-substituts/"><u>Maximiser Les Capacités De Copie Robotique Sous Windows 11: Guide Et Meilleurs Substituts</u></a></li>
<li><a href="https://win-marvelous.techidaily.com/protection-de-disques-durs-avec-mbr-ou-gpt-une-solution-simple-et-efficace/"><u>Protection De Disques Durs Avec MBR Ou GPT : Une Solution Simple Et Efficace</u></a></li>
<li><a href="https://screen-sharing-recording.techidaily.com/quickshot-recorder-evaluation-summary-for-2024/"><u>QuickShot Recorder Evaluation Summary for 2024</u></a></li>
<li><a href="https://win-marvelous.techidaily.com/retrieve-past-document-edits-safely-avoid-data-corruption-tips-and-tricks/"><u>Retrieve Past Document Edits Safely, Avoid Data Corruption Tips and Tricks</u></a></li>
<li><a href="https://tech-revival.techidaily.com/top-video-formats-for-optimal-downloads-on-youtube-in-2020/"><u>Top Video Formats for Optimal Downloads on YouTube in 2020</u></a></li>
<li><a href="https://solve-howtos.techidaily.com/unlocking-the-perfect-algorithm-your-ultimate-guide/"><u>Unlocking the Perfect Algorithm: Your Ultimate Guide</u></a></li>
<li><a href="https://win-marvelous.techidaily.com/windows-11-disk-clutter-solutions-discover-the-top-14-ways-to-free-up-space/"><u>Windows 11 Disk Clutter Solutions: Discover the Top 14 Ways to Free Up Space</u></a></li>
</ul></div>

<!-- affiliate ads begin -->
<iframe width="560" height="315" src="https://www.youtube.com/embed/XIUatTFH0Zw?si=ZCtoBtIy18y2F5Vc" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
<!-- affiliate ads end -->


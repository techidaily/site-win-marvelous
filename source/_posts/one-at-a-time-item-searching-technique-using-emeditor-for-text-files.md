---
title: One-at-a-Time Item Searching Technique Using EmEditor for Text Files
date: 2024-10-24T21:03:52.849Z
updated: 2024-10-28T21:34:13.401Z
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
<li><a href="https://screen-recording.techidaily.com/new-2024-approved-premium-enhancements-guide-to-superior-terria/"><u>[New] 2024 Approved Premium Enhancements Guide to Superior Terria</u></a></li>
<li><a href="https://tiktok-videos.techidaily.com/new-chortling-chronicles-new-comedy-sensations-on-tiktok/"><u>[New] Chortling Chronicles New Comedy Sensations on TikTok</u></a></li>
<li><a href="https://some-guidance.techidaily.com/updated-unveiling-top-templates-for-tiktok-videos/"><u>[Updated] Unveiling Top Templates for TikTok Videos</u></a></li>
<li><a href="https://win-marvelous.techidaily.com/1-schnelles-und-einfaches-sicherstellen-ihrer-daten-mit-wd-mycloud-externe-festplatten-backup-anleitung/"><u>1. Schnelles Und Einfaches Sicherstellen Ihrer Daten Mit WD MyCloud - Externe Festplatten-Backup-Anleitung</u></a></li>
<li><a href="https://win-marvelous.techidaily.com/comment-effacer-en-toute-securite-et-permanence-vos-donnees-sur-un-ssd-de-la-marque-samsung/"><u>Comment Effacer en Toute Sécurité Et Permanence Vos Données Sur Un SSD De La Marque Samsung</u></a></li>
<li><a href="https://win-able.techidaily.com/conquering-darkness-the-ultimate-guide-for-banishing-minecrafts-2024-screen-blackouts/"><u>Conquering Darkness: The Ultimate Guide for Banishing Minecraft's 2024 Screen Blackouts</u></a></li>
<li><a href="https://win-marvelous.techidaily.com/effective-ways-to-tackle-elevated-disk-consumption-from-antimalware-service-exe/"><u>Effective Ways to Tackle Elevated Disk Consumption From Antimalware Service Exe</u></a></li>
<li><a href="https://win-marvelous.techidaily.com/effortless-and-free-solutions-for-protecting-and-copying-your-xbox-consoles-save-data/"><u>Effortless & Free Solutions for Protecting and Copying Your Xbox Console's Save Data</u></a></li>
<li><a href="https://win-marvelous.techidaily.com/geavanceerde-tips-voor-uitwisseling-van-wechat-geschiedenis-vanaf-android-opschreiden-op-ios/"><u>Geavanceerde Tips Voor Uitwisseling Van WeChat Geschiedenis Vanaf Android Opschreiden Op iOS</u></a></li>
<li><a href="https://buynow-reviews.techidaily.com/how-the-modestly-priced-fitbit-versa-stacks-up-against-other-smartwatches/"><u>How the Modestly Priced Fitbit Versa Stacks Up Against Other Smartwatches</u></a></li>
<li><a href="https://article-tips.techidaily.com/in-2024-the-art-of-visual-communication-video-creation-techniques-in-windows-10/"><u>In 2024, The Art of Visual Communication Video Creation Techniques in Windows 10</u></a></li>
<li><a href="https://win-marvelous.techidaily.com/retrieve-past-document-edits-safely-avoid-data-corruption-tips-and-tricks/"><u>Retrieve Past Document Edits Safely, Avoid Data Corruption Tips and Tricks</u></a></li>
<li><a href="https://tiktok-clips.techidaily.com/snapshot-preservation-android-and-mac-techniques/"><u>Snapshot Preservation Android & Mac Techniques</u></a></li>
<li><a href="https://win11-tips.techidaily.com/tackling-w10w11s-err0r-x7e1-issue/"><u>Tackling W10/W11's Err0r: X7E1 Issue</u></a></li>
<li><a href="https://android-unlock.techidaily.com/top-12-prominent-vivo-y27-4g-fingerprint-not-working-solutions-by-drfone-android/"><u>Top 12 Prominent Vivo Y27 4G Fingerprint Not Working Solutions</u></a></li>
<li><a href="https://win-marvelous.techidaily.com/1728478823911-windows-10/"><u>Windows 10无尽解决手段：捷克操作重获突然消失资料技巧</u></a></li>
<li><a href="https://win-marvelous.techidaily.com/windows-11-disk-clutter-solutions-discover-the-top-14-ways-to-free-up-space/"><u>Windows 11 Disk Clutter Solutions: Discover the Top 14 Ways to Free Up Space</u></a></li>
</ul></div>

<!-- affiliate ads begin -->
<a href="https://appsumo.8odi.net/c/5597632/2137413/7443" target="_top" id="2137413">
  <img src="//a.impactradius-go.com/display-ad/7443-2137413" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://appsumo.8odi.net/i/5597632/2137413/7443" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->


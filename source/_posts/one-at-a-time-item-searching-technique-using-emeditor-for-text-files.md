---
title: One-at-a-Time Item Searching Technique Using EmEditor for Text Files
date: 2025-02-13T00:33:54.738Z
updated: 2025-02-19T09:28:10.341Z
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
<li><a href="https://article-posts.techidaily.com/new-2024-approved-from-dull-to-dynamic-top-11-techniques-for-enhanced-hues/"><u>[New] 2024 Approved From Dull to Dynamic Top 11 Techniques for Enhanced Hues</u></a></li>
<li><a href="https://fox-glue.techidaily.com/updated-discover-best-android-picture-tools/"><u>[Updated] Discover Best Android Picture Tools</u></a></li>
<li><a href="https://youtube-zero.techidaily.com/ed-in-2024-stepwise-integration-technique-for-youtube-playlists-on-web/"><u>[Updated] In 2024, Stepwise Integration Technique for YouTube Playlists on Web</u></a></li>
<li><a href="https://win-marvelous.techidaily.com/4-effective-techniques-for-smooth-file-transfers-to-external-drives/"><u>4 Effective Techniques for Smooth File Transfers to External Drives</u></a></li>
<li><a href="https://win-marvelous.techidaily.com/best-folder-copying-solutions-unveiled-plus-detailed-setup-tutorial-for-easy-mastery/"><u>Best Folder Copying Solutions Unveiled + Detailed Setup Tutorial for Easy Mastery</u></a></li>
<li><a href="https://win-marvelous.techidaily.com/comprehensive-guide-on-retrieving-information-from-a-damaged-samsung-external-hard-drive/"><u>Comprehensive Guide on Retrieving Information From a Damaged Samsung External Hard Drive</u></a></li>
<li><a href="https://sim-unlock.techidaily.com/easily-unlock-your-honor-90-device-sim-by-drfone-android/"><u>Easily Unlock Your Honor 90 Device SIM</u></a></li>
<li><a href="https://win-marvelous.techidaily.com/gegevens-groeperen-vervulling-zoekachter-gratis-ontwikkel-het-naar-standaard-op-windows-10/"><u>Gegevens Groeperen Vervulling Zoekachter - Gratis Ontwikkel Het Naar Standaard Op Windows 10</u></a></li>
<li><a href="https://fake-location.techidaily.com/in-2024-11-best-location-changers-for-vivo-g2-drfone-by-drfone-virtual-android/"><u>In 2024, 11 Best Location Changers for Vivo G2 | Dr.fone</u></a></li>
<li><a href="https://some-approaches.techidaily.com/in-2024-tech-jest-crafter/"><u>In 2024, Tech Jest Crafter</u></a></li>
<li><a href="https://youtube-clips.techidaily.com/masterpiece-maker-top-free-editors-for-android-devices/"><u>Masterpiece Maker Top Free Editors for Android Devices</u></a></li>
<li><a href="https://win-marvelous.techidaily.com/page-cannot-be-found-http-404-error-detected/"><u>Page Cannot Be Found - HTTP 404 Error Detected</u></a></li>
<li><a href="https://data-safeguard.techidaily.com/revive-lost-photos-videos-and-contacts-from-your-iphone-using-advanced-data-recovery-for-mac/"><u>Revive Lost Photos, Videos & Contacts From Your iPhone Using Advanced Data Recovery for Mac</u></a></li>
<li><a href="https://tech-renaissance.techidaily.com/top-11-unmissable-last-minute-christmas-shopping-bargains-featured/"><u>Top 11 Unmissable Last-Minute Christmas Shopping Bargains - Featured</u></a></li>
<li><a href="https://win-marvelous.techidaily.com/troubleshooting-and-repairing-windows-nerror-code-0xc000001-expert-tips-and-strategies/"><u>Troubleshooting and Repairing Windows nError Code 0Xc000001: Expert Tips & Strategies</u></a></li>
<li><a href="https://win-marvelous.techidaily.com/ultimate-troubleshooting-tips-unsticking-your-whatsapp-a-comprehensive-walkthrough/"><u>Ultimate Troubleshooting Tips: Unsticking Your WhatsApp - A Comprehensive Walkthrough</u></a></li>
</ul></div>

<!-- affiliate ads begin -->
<iframe width="560" height="315" src="https://www.youtube.com/embed/j5gTm5KxtQ0?si=onF1rBS2nEM5nLGg" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
<!-- affiliate ads end -->


---
title: One-at-a-Time Item Searching Technique Using EmEditor for Text Files
date: 2024-11-11T00:29:31.053Z
updated: 2024-11-12T19:05:12.491Z
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
<li><a href="https://fox-blue.techidaily.com/new-in-2024-enhance-visual-impact-crafting-3d-text-in-photo/"><u>[New] In 2024, Enhance Visual Impact Crafting 3D Text in PHOTO</u></a></li>
<li><a href="https://instagram-videos.techidaily.com/new-insta-cinematography-tips-three-way-borders-for-2024/"><u>[New] Insta Cinematography Tips Three-Way Borders for 2024</u></a></li>
<li><a href="https://screen-capture.techidaily.com/updated-2024-approved-best-screen-recording-software-top-10-list/"><u>[Updated] 2024 Approved Best Screen Recording Software Top 10 List</u></a></li>
<li><a href="https://screen-sharing-recording.techidaily.com/updated-2024-approved-the-great-debate-continues-is-bandicam-or-camtasia-better/"><u>[Updated] 2024 Approved The Great Debate Continues Is Bandicam or Camtasia Better?</u></a></li>
<li><a href="https://tiktok-videos.techidaily.com/updated-pioneer-your-personal-brand-in-tiktok-with-dynamic-backgrounds-for-2024/"><u>[Updated] Pioneer Your Personal Brand in TikTok with Dynamic Backgrounds for 2024</u></a></li>
<li><a href="https://win-marvelous.techidaily.com/windows-11-c3/"><u>輕鬆改良 Windows 11 C分量容量：3 項高效技術指南</u></a></li>
<li><a href="https://win-marvelous.techidaily.com/1728504167884-ssd/"><u>如何在 SSD 重置后迅速检索数据?」</u></a></li>
<li><a href="https://techtrends.techidaily.com/expert-tips-to-correctly-handle-directinput-and-directx-dll-faults-in-windows/"><u>Expert Tips to Correctly Handle Directinput and DirectX Dll Faults in Windows</u></a></li>
<li><a href="https://win-marvelous.techidaily.com/guide-pratique-pour-le-transfert-de-donnees-dhdd-a-ssd-avec-windows-10-des-etapes-faciles-et-economiques/"><u>Guide Pratique Pour Le Transfert De Données D'HDD À SSD Avec Windows 10: Des Étapes Faciles Et Économiques</u></a></li>
<li><a href="https://win-marvelous.techidaily.com/how-to-resolve-iphone-whatsapp-backup-failures-top-9-strategies-unveiled/"><u>How to Resolve iPhone WhatsApp Backup Failures: Top 9 Strategies Unveiled</u></a></li>
<li><a href="https://win-marvelous.techidaily.com/logiciels-incontournables-pour-cloner-votre-ssd-corsair-le-choix-du-n1-en-securite-et-performance/"><u>Logiciels Incontournables Pour Cloner Votre SSD Corsair : Le Choix Du N°1 en Sécurité Et Performance</u></a></li>
<li><a href="https://some-skills.techidaily.com/the-ultimate-tally-unveiling-the-highest-rated-threads-on-reddit-for-2024/"><u>The Ultimate Tally Unveiling the Highest-Rated Threads on Reddit for 2024</u></a></li>
<li><a href="https://program-issues.techidaily.com/troubleshoot-inaccessible-camera-problem-on-snap-effective-tips/"><u>Troubleshoot Inaccessible Camera Problem on Snap: Effective Tips</u></a></li>
<li><a href="https://win-marvelous.techidaily.com/ultimate-guide-top-rated-software-for-thoroughly-wiping-your-hard-drive-and-operating-system/"><u>Ultimate Guide: Top Rated Software for Thoroughly Wiping Your Hard Drive & Operating System</u></a></li>
<li><a href="https://win-marvelous.techidaily.com/voorlopige-oplossingen-voor-het-herstellen-van-uw-iphone-de-kracht-van-icloud-back-ups-in-achtergrond/"><u>Voorlopige Oplossingen Voor Het Herstellen Van Uw iPhone: De Kracht Van iCloud Back-Ups In Achtergrond</u></a></li>
</ul></div>

<!-- affiliate ads begin -->
<a href="https://aligracehair.sjv.io/c/5597632/2135393/19272" target="_top" id="2135393">
  <img src="//a.impactradius-go.com/display-ad/19272-2135393" border="0" alt="https://techidaily.com" width="120" height="90"/>
</a>
<img height="0" width="0" src="https://aligracehair.sjv.io/i/5597632/2135393/19272" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->


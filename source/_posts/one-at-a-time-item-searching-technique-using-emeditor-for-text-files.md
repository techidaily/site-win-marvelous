---
title: One-at-a-Time Item Searching Technique Using EmEditor for Text Files
date: 2024-10-21T19:32:35.204Z
updated: 2024-10-22T18:27:48.329Z
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
<li><a href="https://facebook-video-footage.techidaily.com/new-day-jobs-and-digital-passion-striking-a-balance-for-2024/"><u>[New] Day Jobs & Digital Passion Striking a Balance for 2024</u></a></li>
<li><a href="https://extra-skills.techidaily.com/new-iphoneandroids-top-sticker-adding-apps-the-essential-10-collection/"><u>[New] IPhone/Android's Top Sticker-Adding Apps The Essential 10 Collection</u></a></li>
<li><a href="https://vp-tips.techidaily.com/new-premier-tools-upload-and-convert-vids-for-tweeting-for-2024/"><u>[New] Premier Tools Upload & Convert Vids for Tweeting for 2024</u></a></li>
<li><a href="https://screen-video-capture.techidaily.com/updated-2024-approved-transform-virtual-engagements-the-10-free-applications-you-need/"><u>[Updated] 2024 Approved Transform Virtual Engagements The 10 Free Applications You Need</u></a></li>
<li><a href="https://fox-blue.techidaily.com/updated-faqs-of-using-vlc-player-on-mac/"><u>[Updated] FAQs of Using VLC Player on Mac</u></a></li>
<li><a href="https://vp-tips.techidaily.com/updated-in-2024-top-8-4k-playback-powerhouses-unveiled/"><u>[Updated] In 2024, Top 8 4K Playback Powerhouses Unveiled</u></a></li>
<li><a href="https://win-marvelous.techidaily.com/1728508672603-4/"><u>「エクスプローラ - 急速にアクセス不能となった！これらの4手順ですぐに使用可能に」</u></a></li>
<li><a href="https://digital-screen-recording.techidaily.com/2024-approved-advanced-techniques-developing-elapsed-time-features-in-obs-software/"><u>2024 Approved Advanced Techniques Developing Elapsed Time Features in OBS Software</u></a></li>
<li><a href="https://win-marvelous.techidaily.com/1728484083537-windows-server/"><u>信頼できるバックアップソフトを探す:Windows Server用ベストリスト</u></a></li>
<li><a href="https://win-marvelous.techidaily.com/comparing-wd-backup-and-windows-backup-which-one-provides-superior-data-protection/"><u>Comparing WD Backup and Windows Backup: Which One Provides Superior Data Protection?</u></a></li>
<li><a href="https://win-marvelous.techidaily.com/diskpart-clean-command-successfully-resolved-error-fix-tips/"><u>DiskPart Clean Command Successfully Resolved: Error Fix Tips</u></a></li>
<li><a href="https://win-marvelous.techidaily.com/effortless-windows-nt-transition-to-solid-state-drives-with-no-resizing-needed-best-strategies-explained/"><u>Effortless Windows nT Transition to Solid State Drives with No Resizing Needed: Best Strategies Explained</u></a></li>
<li><a href="https://android-pokemon-go.techidaily.com/in-2024-preparation-to-beat-giovani-in-pokemon-go-for-oppo-find-x6-pro-drfone-by-drfone-virtual-android/"><u>In 2024, Preparation to Beat Giovani in Pokemon Go For Oppo Find X6 Pro | Dr.fone</u></a></li>
<li><a href="https://win-marvelous.techidaily.com/le-meilleur-logiciel-de-sauvegarde-et-recuperation-pour-seagate-backup-plus-portable-5-tb-criteres-devaluation/"><u>Le Meilleur Logiciel De Sauvegarde Et Récupération Pour Seagate Backup Plus Portable 5 TB: Critères D'Évaluation</u></a></li>
<li><a href="https://win-marvelous.techidaily.com/1728492165033-ps4/"><u>PS4初回起動後でも安全にゲームデータ復元方法</u></a></li>
<li><a href="https://win-marvelous.techidaily.com/step-by-step-guide-transferring-your-iphones-contact-list-into-a-csv-vcf-or-excel-file/"><u>Step-by-Step Guide: Transferring Your iPhone's Contact List Into a CSV, VCF, or Excel File</u></a></li>
<li><a href="https://some-tips.techidaily.com/top-10-traffic-cams-for-superior-vehicle-tracking-for-2024/"><u>Top 10 Traffic Cams for Superior Vehicle Tracking for 2024</u></a></li>
<li><a href="https://extra-hints.techidaily.com/unveiling-top-online-markets-for-quality-tamil-ringtone-downloads/"><u>Unveiling Top Online Markets for Quality Tamil Ringtone Downloads</u></a></li>
<li><a href="https://win-marvelous.techidaily.com/zeitgesteuerte-ubertragung-von-dokumenten-in-einen-alternativen-verzeichnisplatz/"><u>Zeitgesteuerte Übertragung Von Dokumenten in Einen Alternativen Verzeichnisplatz</u></a></li>
</ul></div>

<!-- affiliate ads begin -->
<a href="https://aligracehair.sjv.io/c/5597632/2135365/19272" target="_top" id="2135365">
  <img src="//a.impactradius-go.com/display-ad/19272-2135365" border="0" alt="https://techidaily.com" width="125" height="90"/>
</a>
<img height="0" width="0" src="https://aligracehair.sjv.io/i/5597632/2135365/19272" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->


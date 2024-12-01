---
title: One-at-a-Time Item Searching Technique Using EmEditor for Text Files
date: 2024-11-24T23:54:25.337Z
updated: 2024-12-01T03:57:05.884Z
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
<li><a href="https://fox-friendly.techidaily.com/new-2024-approved-ultimate-mobile-and-web-photo-booster-at-no-cost/"><u>[New] 2024 Approved Ultimate Mobile & Web Photo Booster at No Cost</u></a></li>
<li><a href="https://fox-boxes.techidaily.com/updated-2024-approved-what-to-expect-from-the-dji-inspire-2-experience/"><u>[Updated] 2024 Approved What to Expect From the DJI Inspire 2 Experience</u></a></li>
<li><a href="https://win-marvelous.techidaily.com/3windowschk/"><u>3個高效解決辦法：如何將Windows電腦中遭忘記的CHK檔案重新恢復</u></a></li>
<li><a href="https://fox-ssl.techidaily.com/effizientes-upgrade-von-mainboards-und-cpus-unter-beibehaltung-der-vorhandenen-windows-betriebssystemversion-windows-11-10-8/"><u>Effizientes Upgrade Von Mainboards Und CPUs Unter Beibehaltung Der Vorhandenen Windows-Betriebssystemversion (Windows 11, 10, 8,</u></a></li>
<li><a href="https://win-marvelous.techidaily.com/ferramentas-livres-para-implantar-solucoes-de-clonagem-de-rede-e-manipulacao-de-imagens/"><u>Ferramentas Livres Para Implantar Soluções De Clonagem De Rede E Manipulação De Imagens</u></a></li>
<li><a href="https://blog-min.techidaily.com/how-to-repair-excel-file-name-is-not-valid-error-by-stellar-guide/"><u>How to Repair Excel File Name is Not Valid Error</u></a></li>
<li><a href="https://android-unlock.techidaily.com/in-2024-how-to-remove-a-previously-synced-google-account-from-your-sony-xperia-10-v-by-drfone-android/"><u>In 2024, How to Remove a Previously Synced Google Account from Your Sony Xperia 10 V</u></a></li>
<li><a href="https://iphone-unlock.techidaily.com/in-2024-unlock-iphone-14-pro-max-with-forgotten-passcode-different-methods-you-can-try-drfone-by-drfone-ios/"><u>In 2024, Unlock iPhone 14 Pro Max With Forgotten Passcode Different Methods You Can Try | Dr.fone</u></a></li>
<li><a href="https://vp-tips.techidaily.com/masterfulaiimageeditor-the-best-of-both-worlds-for-2024/"><u>MasterfulAiImageEditor The Best of Both Worlds for 2024</u></a></li>
<li><a href="https://win-marvelous.techidaily.com/quick-solutions-to-resolve-windows-11-download-folder-non-responsive-error/"><u>Quick Solutions to Resolve 'Windows 11 Download Folder Non-Responsive' Error</u></a></li>
<li><a href="https://win-marvelous.techidaily.com/transferir-archivos-de-ssd-a-hdd-con-facilidad-guia-para-windows-11/"><u>Transferir Archivos De SSD a HDD Con Facilidad: Guía Para Windows 11</u></a></li>
<li><a href="https://win-marvelous.techidaily.com/ultimate-guide-starting-up-with-external-media-lenovo-pcs-and-windows-11/"><u>Ultimate Guide: Starting Up With External Media - Lenovo PCs & Windows 11</u></a></li>
<li><a href="https://screen-video-capture.techidaily.com/ultimate-list-of-low-cost-desktop-encoder-software/"><u>Ultimate List of Low-Cost Desktop Encoder Software</u></a></li>
<li><a href="https://win-marvelous.techidaily.com/youtube-satara-ka-anarapa-4-takanaya-ma-khajana-val-khaja-btha-fiil/"><u>Youtube स्टोरी के अनुरूप, 4 तकनीयों में खोजने वाले खोज बिंदु: फ़ाइलें</u></a></li>
</ul></div>

<!-- affiliate ads begin -->
<iframe width="560" height="315" src="https://www.youtube.com/embed/RJNYTGHVlLc?si=lhdUUVYMVQjzHXBh" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
<!-- affiliate ads end -->


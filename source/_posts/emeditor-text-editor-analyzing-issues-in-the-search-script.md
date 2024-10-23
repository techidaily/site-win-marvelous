---
title: "EmEditor Text Editor: Analyzing Issues in the Search Script"
date: 2024-10-20T22:21:38.487Z
updated: 2024-10-23T04:03:31.646Z
tags:
  - product
categories:
  - emeditor
thumbnail: https://thmb.techidaily.com/5e307eed611f17e095f5d88028b2351fba3d967d59553e6950da1a4414daed51.jpg
---

## EmEditor Text Editor: Analyzing Issues in the Search Script

Viewing 2 posts - 1 through 2 (of 2 total)

* Author  
Posts
* October 26, 2007 at 9:17 am [#4859](https://tools.techidaily.com/emeditor/products/)  
[![](https://secure.gravatar.com/avatar/e4b3430962364a05c69af317cc2183cf?s=80&d=identicon&r=g)QiaoJiao](https://www.emeditor.com/forums/users/QiaoJiao/ "View QiaoJiao's profile")  
Participant  
Please, say what is wrong with that search script:  
 editor.FindInFiles(“xxx”, “C:web\*.txt”, eeOpenDetectUTF8, eeEncodingSystemDefault);  
 It returns error  
Wrong number of arguments or invalid property assignment  
 I can not figer out where mistake is.  
October 27, 2007 at 12:35 am [#4861](https://tools.techidaily.com/emeditor/products/)  
[![](https://secure.gravatar.com/avatar/a0a6377144ed3636f985d87303f65ed2?s=80&d=identicon&r=g)Yutaka Emura](https://www.emeditor.com/forums/users/yemura/ "View Yutaka Emura's profile")  
Keymaster  
You will need the last parameter _strFilesToIgnore_.  
 So the correct code is:  
    
	editor.FindInFiles("xxx", "C:web*.txt", eeOpenDetectUTF8, eeEncodingSystemDefault, "");
* Author  
Posts

Viewing 2 posts - 1 through 2 (of 2 total)

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
<li><a href="https://article-files.techidaily.com/new-building-your-dream-4k-video-editing-studio-a-diy-blueprint-for-2024/"><u>[New] Building Your Dream 4K Video Editing Studio A DIY Blueprint for 2024</u></a></li>
<li><a href="https://youtube-blog.techidaily.com/n-2024-pros-recommendations-leading-video-editing-software/"><u>[New] In 2024, Pros' Recommendations Leading Video Editing Software</u></a></li>
<li><a href="https://screen-capture.techidaily.com/new-in-2024-screen-savvy-the-ultimate-recorders-digest/"><u>[New] In 2024, Screen Savvy The Ultimate Recorder's Digest</u></a></li>
<li><a href="https://win-marvelous.techidaily.com/1-access-restored-enhancing-your-icloud-music-library-functionality/"><u>1. Access Restored: Enhancing Your iCloud Music Library Functionality</u></a></li>
<li><a href="https://technical-tips.techidaily.com/apple-and-samsung-unveil-the-true-test-of-microsofts-artificial-intelligence-prowess-the-surprise-factor/"><u>Apple & Samsung Unveil the True Test of Microsoft’s Artificial Intelligence Prowess – The Surprise Factor!</u></a></li>
<li><a href="https://win-marvelous.techidaily.com/die-top-tipps-zur-risikofreien-einrichtung-einer-windows-cf-karte-kostenlos-verfugbar-machen/"><u>Die Top-Tipps Zur Risikofreien Einrichtung Einer Windows CF Karte Kostenlos Verfügbar Machen</u></a></li>
<li><a href="https://some-knowledge.techidaily.com/1725284478607-dvd-dvd/"><u>DVDコピー・リッピング手順について学ぶ |合法的な方法でDVDのバックアップを作成</u></a></li>
<li><a href="https://youtube-zero.techidaily.com/ational-steps-for-youtube-enthusiasts-for-2024/"><u>Foundational Steps for YouTube Enthusiasts for 2024</u></a></li>
<li><a href="https://win-marvelous.techidaily.com/how-to-recover-unseen-images-from-your-icloud-backup-a-step-by-step-guide-6-methods/"><u>How to Recover Unseen Images From Your iCloud Backup: A Step-by-Step Guide (6 Methods)</u></a></li>
<li><a href="https://easy-unlock-android.techidaily.com/how-to-unlock-motorola-edge-2023-phone-without-password-by-drfone-android/"><u>How To Unlock Motorola Edge 2023 Phone Without Password?</u></a></li>
<li><a href="https://sim-unlock.techidaily.com/in-2024-the-best-android-unlock-software-for-oppo-k11x-device-top-5-picks-to-remove-android-locks-by-drfone-android/"><u>In 2024, The Best Android Unlock Software For Oppo K11x Device Top 5 Picks to Remove Android Locks</u></a></li>
<li><a href="https://win-marvelous.techidaily.com/investigando-las-profundidades-una-guia-para-explorar-en-imagen/"><u>Investigando Las Profundidades: Una Guía Para Explorar en Imagen</u></a></li>
<li><a href="https://win-marvelous.techidaily.com/reparacion-de-la-particion-efi-borrada-en-windows-10-dos-metodos-efectivos/"><u>Reparación De La Partición EFI Borrada en Windows 10: Dos Métodos Efectivos</u></a></li>
<li><a href="https://win-marvelous.techidaily.com/sauvegarde-sans-frais-logiciel-de-sauvegarde-incrementale-et-differentielle-avec-aomei/"><u>Sauvegarde Sans Frais: Logiciel De Sauvegarde Incrémentale Et Différentielle Avec AOMEI</u></a></li>
</ul></div>

<!-- affiliate ads begin -->
<a href="https://aligracehair.sjv.io/c/5597632/1938750/19272" target="_top" id="1938750">
  <img src="//a.impactradius-go.com/display-ad/19272-1938750" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://aligracehair.sjv.io/i/5597632/1938750/19272" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->


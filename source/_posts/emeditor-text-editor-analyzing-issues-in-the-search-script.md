---
title: "EmEditor Text Editor: Analyzing Issues in the Search Script"
date: 2024-11-21T02:36:43.680Z
updated: 2024-11-22T23:10:17.451Z
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
<li><a href="https://some-techniques.techidaily.com/new-hue-harmony-simplified-steps-for-professional-color-adjustment/"><u>[New] Hue Harmony Simplified Steps for Professional Color Adjustment</u></a></li>
<li><a href="https://ai-vdieo-software.techidaily.com/2024-approved-rip-and-convert-a-step-by-step-guide-to-digitizing-your-dvds/"><u>2024 Approved Rip & Convert A Step-by-Step Guide to Digitizing Your DVDs</u></a></li>
<li><a href="https://media-tips.techidaily.com/decoding-audio-file-types-understanding-the-distinct-characteristics-of-aiff-wav-flac-and-alac/"><u>Decoding Audio File Types: Understanding the Distinct Characteristics of AIFF, WAV, FLAC & ALAC</u></a></li>
<li><a href="https://win-marvelous.techidaily.com/effective-techniques-for-ssd-partition-restoration/"><u>Effective Techniques for SSD Partition Restoration</u></a></li>
<li><a href="https://win-marvelous.techidaily.com/einfachere-methode-zur-erstellung-von-netzwerk-system-backups-mit-aomei-backupper-auf-windows/"><u>Einfachere Methode Zur Erstellung Von Netzwerk-System-Backups Mit AOMEI Backupper Auf Windows</u></a></li>
<li><a href="https://win-marvelous.techidaily.com/estrategias-faciles-de-seguir-para-desbloquear-tus-datos-en-memorias-extras/"><u>Estrategias Fáciles De Seguir Para Desbloquear Tus Datos en Memorias Extras</u></a></li>
<li><a href="https://win-marvelous.techidaily.com/how-to-fix-cant-make-restore-points-in-windows-11-top-4-solutions/"><u>How To Fix 'Can't Make Restore Points In Windows 11', Top 4 Solutions</u></a></li>
<li><a href="https://extra-information.techidaily.com/in-2024-canons-lut-collection-maximize-image-impact-free-and-paid-choices/"><u>In 2024, Canon’s LUT Collection Maximize Image Impact - FREE & Paid Choices</u></a></li>
<li><a href="https://sim-unlock.techidaily.com/in-2024-the-best-android-unlock-software-for-xiaomi-mix-fold-3-device-top-5-picks-to-remove-android-locks-by-drfone-android/"><u>In 2024, The Best Android Unlock Software For Xiaomi Mix Fold 3 Device Top 5 Picks to Remove Android Locks</u></a></li>
<li><a href="https://win-marvelous.techidaily.com/methodes-efficaces-pour-restaurer-des-fichiers-effaces-sur-un-lecteur-partage-windows-une-approche-detaillee/"><u>Méthodes Efficaces Pour Restaurer Des Fichiers Effacés Sur Un Lecteur Partagé Windows : Une Approche Détaillée</u></a></li>
<li><a href="https://win-dash.techidaily.com/quick-download-hp-stream-device-driver-software/"><u>Quick Download: HP Stream Device Driver Software</u></a></li>
<li><a href="https://techidaily.com/remove-google-frp-lock-on-poco-x6-by-drfone-android-unlock-remove-google-frp/"><u>Remove Google FRP lock on Poco X6</u></a></li>
<li><a href="https://win-marvelous.techidaily.com/windows-server-2016-resolving-issues-with-failed-system-state-backups/"><u>Windows Server 2016 - Resolving Issues with Failed System State Backups</u></a></li>
</ul></div>

<!-- affiliate ads begin -->
<iframe width="560" height="315" src="https://www.youtube.com/embed/f3PFn06LijE?si=zHrmlTOzrKxXe-k4&autoplay=1" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
<!-- affiliate ads end -->


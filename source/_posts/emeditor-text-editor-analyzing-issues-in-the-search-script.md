---
title: "EmEditor Text Editor: Analyzing Issues in the Search Script"
date: 2024-11-23T17:57:10.720Z
updated: 2024-12-01T06:50:49.029Z
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
<li><a href="https://facebook-videos.techidaily.com/updated-2024-approved-enhancing-engagement-the-art-of-animated-fb-advertising/"><u>[Updated] 2024 Approved Enhancing Engagement The Art of Animated FB Advertising</u></a></li>
<li><a href="https://discover-cheats.techidaily.com/comment-configurer-la-sauvegarde-automatique-de-gmail-avantages-et-etapes-pratiques/"><u>Comment Configurer La Sauvegarde Automatique De Gmail: Avantages Et Étapes Pratiques</u></a></li>
<li><a href="https://discover-extraordinary.techidaily.com/descubre-las-siete-estrategias-clave-para-un-optimizacion-de-motores-de-busqueda-seo-exitosa/"><u>Descubre Las Siete Estrategias Clave Para Un Optimización De Motores De Búsqueda (SEO) Exitosa</u></a></li>
<li><a href="https://win-marvelous.techidaily.com/fast-und-sicher-vier-methoden-zum-hochladen-iphones-songs-auf-den-computer/"><u>Fast Und Sicher - Vier Methoden Zum Hochladen iPhones Songs Auf Den Computer</u></a></li>
<li><a href="https://instagram-videos.techidaily.com/in-2024-prime-hash-monitoring-apps-for-social-media-giants-fb-tweetinsta/"><u>In 2024, Prime Hash Monitoring Apps for Social Media Giants (FB, Tweet/Insta)</u></a></li>
<li><a href="https://win-marvelous.techidaily.com/leading-lightweight-windows-defense-suites-the-ultimate-guide-to-portable-security-programs/"><u>Leading Lightweight Windows Defense Suites: The Ultimate Guide to Portable Security Programs</u></a></li>
<li><a href="https://win-marvelous.techidaily.com/mastering-synology-nas-backup-the-best-3-approaches-for-incremental-data-protection/"><u>Mastering Synology NAS Backup: The Best 3 Approaches for Incremental Data Protection</u></a></li>
<li><a href="https://win-marvelous.techidaily.com/schritt-fur-schritt-anleitung-zur-nutzung-von-windows-7s-integriertem-wbadmin-fur-zuverlassige-datenwiederherstellung/"><u>Schritt-Für-Schritt-Anleitung Zur Nutzung Von Windows 7S Integriertem WBAdmin Für Zuverlässige Datenwiederherstellung</u></a></li>
<li><a href="https://some-knowledge.techidaily.com/streamline-video-management-in-winxvideo-using-tutorai-tips-for-recording-editing-and-compression/"><u>Streamline Video Management in WinXVideo Using TutorAI - Tips for Recording, Editing & Compression</u></a></li>
<li><a href="https://win-marvelous.techidaily.com/transferer-vos-donnees-samsung-avec-facilite-comment-migrer-sur-une-nouvelle-memoire-ssd-samsung/"><u>Transférer Vos Données Samsung Avec Facilité - Comment Migrer Sur Une Nouvelle Mémoire SSD Samsung ?</u></a></li>
<li><a href="https://article-knowledge.techidaily.com/voters-victories-reddits-most-popular-threads-top-10/"><u>Voters' Victories Reddit’s Most Popular Threads (Top 10)</u></a></li>
<li><a href="https://hardware-tips.techidaily.com/zdnets-must-skip-apple-picks-the-4-items-to-avoid-in-todays-market/"><u>ZDNet's Must-Skip Apple Picks: The 4 Items to Avoid in Today's Market</u></a></li>
</ul></div>

<!-- affiliate ads begin -->
<iframe width="560" height="315" src="https://www.youtube.com/embed/BmegThMdrJE?si=rILo1FJb9DgnPljV" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
<!-- affiliate ads end -->


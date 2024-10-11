---
title: "EmEditor Text Editor: Analyzing Issues in the Search Script"
date: 2024-10-09T16:05:14.966Z
updated: 2024-10-11T16:37:36.535Z
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
<li><a href="https://extra-tips.techidaily.com/2024-approved-best-aspect-ratios-to-enhance-video-quality/"><u>2024 Approved Best Aspect Ratios to Enhance Video Quality</u></a></li>
<li><a href="https://discover-alternatives.techidaily.com/1726028396513-mp4-avi-movbmp/"><u>動画の互換性向上: MP4, AVI, MOVからBMPへのスムーズな変換テクニック</u></a></li>
<li><a href="https://blog-min.techidaily.com/1725285855008-avi-mp4/"><u>转换 AVI 文件到 MP4 以免费 - 前八个有效方法</u></a></li>
<li><a href="https://tech-hub.techidaily.com/assistive-algorithms-for-algebra-problems/"><u>Assistive Algorithms for Algebra Problems</u></a></li>
<li><a href="https://ios-unlock.techidaily.com/how-do-you-remove-restricted-mode-on-iphone-7-plus-by-drfone-ios/"><u>How Do You Remove Restricted Mode on iPhone 7 Plus</u></a></li>
<li><a href="https://blog-min.techidaily.com/how-to-oneplus-get-deleted-photos-back-with-ease-and-safety-by-fonelab-android-recover-photos/"><u>How to OnePlus Get Deleted photos Back with Ease and Safety?</u></a></li>
<li><a href="https://android-pokemon-go.techidaily.com/in-2024-ultimate-guide-to-catch-the-regional-located-pokemon-for-itel-p55-drfone-by-drfone-virtual-android/"><u>In 2024, Ultimate Guide to Catch the Regional-Located Pokemon For Itel P55 | Dr.fone</u></a></li>
<li><a href="https://win-marvelous.techidaily.com/solve-your-video-playback-problems-on-youtube-easily/"><u>Solve Your Video Playback Problems on YouTube Easily</u></a></li>
<li><a href="https://win-marvelous.techidaily.com/step-by-step-guide-downloading-shutterstock-footage-from-pc-or-mac/"><u>Step-by-Step Guide: Downloading Shutterstock Footage From PC or Mac</u></a></li>
<li><a href="https://win-marvelous.techidaily.com/step-by-step-tutorial-access-and-use-spotify-on-an-iphone-or-ipad/"><u>Step-by-Step Tutorial: Access and Use Spotify on an iPhone or iPad</u></a></li>
<li><a href="https://win-marvelous.techidaily.com/top-alternatives-to-flvto-enhance-your-video-conversions/"><u>Top Alternatives to FLVTO: Enhance Your Video Conversions</u></a></li>
</ul></div>

<!-- affiliate ads begin -->
<a href="https://aligracehair.sjv.io/c/5597632/1975802/19272" target="_top" id="1975802">
  <img src="//a.impactradius-go.com/display-ad/19272-1975802" border="0" alt="https://techidaily.com" width="300" height="90"/>
</a>
<img height="0" width="0" src="https://aligracehair.sjv.io/i/5597632/1975802/19272" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->


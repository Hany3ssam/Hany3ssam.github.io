---
layout: post
title: Binary Search
categories: [Algorithms]
tags: [Algorithms,Binary Search]
description: 
comments:
---

<p >
This is the first post in a series of upcoming Algorithms tutorials, Its very important as a Software Developer to learn and understand Algorithms, for one thing, If you want to join the kick ass companies such as Google,Facebook etc, As they barley question your knowledge of specific programming language or what stack you’re familiar with, rather how you think, your problem solving techniques and how you approach a particular problem, So most of the interview questions will be mainly algorithms based.
The other reason is for you to advance your skills and your problem solving techniques as this is what sets a good developer apart from the other ones.
I can’t emphasis enough how understanding Algorithms is important to you as a software developer.
This tutorial series will be in Arabic language as im sure there are plenty of good resources out there written in English, so this is for our fellow Arabic speaker gurus.</p>
<div dir="rtl">
الأول خلونا نبدأ نتكلم عن الالجوريثم بصفه عامة,
<br>
الألجوريثم هى عبارة عن خطوات بنعملها لحل المشكلات, أو الخطوات اللى بنعملها للوصول لهدف معين, يعنى مثلا اللى ب ي كس اس مديرو ف الشغل عشان يوصل ده بيستخدم طريقه معينه ف الوصول للهدف, أو حد تانى ابن ناس بيشتغل على نفسه و بيجتهد عشان يوصل ده بردو بيستخدم ألجوريثم,
ف الخطوات اللى انت بتعملها عشان تحل مشكله او توصل لهدف هو ده الالجوريثم,  كل ألجوريثم ليها كومبليكستى, و هى مقدار الوقت اللى انت بتاخدوا عشان تحل مشكله او توصل لهدف.  
<p>
<h3>Binary Search</h3>
تخيل كده انك عايز تدور على رقم وسط مجموعه ارقام ف(اراي) مثلا, ف ممكن حضرتك تيجي و تمسك ال اراى دى و تمشى من اول انديكس فيها و تشوف هوا ده الرقم اللى بتدور عليه ؟ لا, طيب شوف اللى بعده, وهكذا لحد لما تلاقى الرقم اللى بتدور عليه, دى طريقه, او الجوريثم(ليـــنر ســيرش) بس مش ظريفه, افرض مثلا ان الاراى اللى بتدور فيها, فيها 100 رقم, و الرقم اللى بتدور عليه ف الاخر, ف انت كده هتضطر تمشى ف الاراى كلها تشوف رقم رقم لحد لما توصل للرقم اللى بتدور عليه, طيب افرض فيها 100 الف رقم؟ مش هياكل صح!
<br>
الباينرى سيرش بقي فكرتها ظريفه نسبيا, انا مش هدور من اول انديكس ف ال أراى, انا هدور من النص, ف خلينا نفترض مثلا ان عندنا أراى فيها 25 ايلمنت, ف هاجى عند ال  
انديكس 12 و اشوف, انت الرقم اللى بدور عليه؟
</p>
<span>
 <img src="https://s3.amazonaws.com/ka-cs-algorithms/primes1.png">
 </span>
 <p>
لا, طيب انت اكبر ولا اصغر من الرقم اللى بدور عليه؟ لو فرضنا انى بدور على الرقم 67, ف هنلاقى ان ال انديكس 12 شايل القيمه 41, ف انت اصغر وش, يبقي انا هستبعد تماما ومش هدور قبل الانديكس 12, هبدأ ادور من انديكس 13
</p>
<span>
<img src="https://s3.amazonaws.com/ka-cs-algorithms/primes2.png">
</span>
<p>
و هكرر الخطوة الاولى اللى عملتها تانى, ( 13 + 24)/2 هيدينى 18, على افتراض اننا بنقرب الى اقرب رقم صحيح, يبقي هشوف ال انديكس 18 انت الرقم اللى بدور عليه ؟ اه , انا بدور على الرقم 67 فعلا.
</p>
<span>
<img src="https://s3.amazonaws.com/ka-cs-algorithms/primes3.png">
</span>
بس, ده ببساطه ال باينرى سيرش, ده طبعا على افتراض ان الأراى مترتبه تصاعديا و الرقم اللى بدور عليه موجود . ده ال سودو كود:
</div>
<p>
<ol>
<li>Let min = 0 and max = n-1.</li>
<li>Compute guess as the average of max and min, rounded down so that it is an integer.</li>
<li>If array[guess] equals target, then stop. You found it! Return guess.</li>
<li>If the guess was too low, that is, array[guess] < target, then set min = guess + 1.</li>
<li>Otherwise, the guess was too high. Set max = guess -1.</li>
<li>Go back to step two.</li>
</ol>
</p>




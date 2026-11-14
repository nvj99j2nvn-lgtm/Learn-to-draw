<!DOCTYPE html>
<html lang="ar" dir="rtl"><head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1, viewport-fit=cover">
<meta name="theme-color" content="#e6e5df">
<title>التأسيس — إيبس باينت من الصفر</title>
<link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Amiri:wght@400;700&family=Anton&family=Cairo:wght@700;900&display=swap">
<style>
:root{color-scheme:light;--bg:#e6e5df;--ink:#161616;--mut:#5d5d5a;--red:#a82a22;--amber:#7d5f1c;--rule:rgba(22,22,22,.6);--line:#c4c2b9;--card:#efeee9}
*{box-sizing:border-box;margin:0;padding:0}
html{scroll-padding-top:60px}
body{background:var(--bg);color:var(--ink);font-family:Amiri,"DejaVu Serif",Tahoma,serif;font-size:19px;line-height:1.75;padding-top:env(safe-area-inset-top,0)}
body::before{content:"";position:fixed;inset:0;pointer-events:none;z-index:0;opacity:.5;background:radial-gradient(circle at 90% -5%,rgba(242,180,90,.10),transparent 40%)}
body::after{content:"";position:fixed;inset:0;pointer-events:none;z-index:0;opacity:.18;background:repeating-linear-gradient(104deg,transparent 0 22px,rgba(180,200,230,.12) 22px 23px,transparent 23px 61px);background-size:100px 400px;animation:rain 3s linear infinite}
@keyframes rain{to{background-position:-40px 400px}}
@media(prefers-reduced-motion:reduce){body::after{animation:none}}
.paper{position:relative;z-index:1;max-width:780px;margin:0 auto;padding:14px 16px 70px}
h1,h2,h3,.hl,.kick,nav button,.btn{font-family:Cairo,"DejaVu Sans",sans-serif}
.strip{display:flex;justify-content:space-between;gap:8px;font:700 12px Cairo,sans-serif;letter-spacing:1px;border-top:1px solid var(--rule);border-bottom:1px solid var(--rule);padding:3px 2px}
.mast{display:flex;align-items:center;justify-content:center;gap:14px;padding:10px 0 6px;border-bottom:4px double var(--rule)}
.mast h1{font-size:clamp(2.2rem,9vw,4.2rem);font-weight:900;line-height:1.15;text-align:center}
.mast img{width:clamp(34px,8vw,54px);height:clamp(34px,8vw,54px);border-radius:6px}
nav{position:sticky;top:0;z-index:20;background:rgba(230,229,223,.94);backdrop-filter:blur(8px);border-bottom:1px solid var(--rule);padding-top:env(safe-area-inset-top,0)}
nav div{display:flex;gap:2px;overflow-x:auto;justify-content:flex-start}
nav button{flex:none;font-weight:700;font-size:15px;color:var(--mut);background:none;border:0;border-bottom:3px solid transparent;padding:8px 12px;cursor:pointer}
nav button.on{color:var(--ink);border-bottom-color:var(--red)}
section{display:none;padding-top:16px}section.on{display:block}
.kick{font-size:13px;font-weight:900;color:var(--red);letter-spacing:1px;margin-bottom:2px}
.hl{font-weight:900;font-size:clamp(1.7rem,6vw,2.5rem);line-height:1.25}
.dek{color:#2a2a2a;margin:4px 0 10px}
figure{margin:10px 0}
figure img{display:block;width:100%;border:1px solid var(--rule);padding:4px;background:var(--card)}
figcaption{font-size:.82rem;color:var(--mut);border-top:1px solid var(--line);margin-top:4px;padding-top:2px}
.dbl{border-top:4px double var(--rule);margin:18px 0 14px}
.cd{display:grid;grid-template-columns:repeat(4,1fr);text-align:center;border:1px solid var(--rule);margin:8px 0}
.cd div{padding:8px 2px;border-left:1px solid var(--line)}.cd div:last-child{border:0}
.cd b{display:block;font:400 clamp(1.8rem,8vw,2.8rem)/1 Anton,Impact,sans-serif;direction:ltr}
.cd span{font:700 12px Cairo,sans-serif;color:var(--mut)}
.bar{height:10px;background:#d3d1c8;border:1px solid var(--rule);margin-top:6px}.bar i{display:block;height:100%;width:0;background:var(--red);transition:width .4s}
.stars{display:flex;gap:8px;margin:10px 0}.stars img{width:30px;height:30px;border-radius:5px;opacity:.2;transition:opacity .3s}.stars img.on{opacity:1}
.form{border:1px solid var(--rule);padding:12px;margin:10px 0;text-align:center}
.yn{display:flex;justify-content:center;gap:34px;margin-top:8px}
.yn button{background:none;border:0;color:var(--ink);font:700 15px Cairo,sans-serif;cursor:pointer;display:grid;gap:4px;justify-items:center}
.yn img{width:64px;height:64px;border-radius:10px;border:1px solid var(--rule)}.yn .x{width:64px;height:64px;border-radius:10px;border:1px solid var(--rule);display:grid;place-items:center;font-size:42px;color:var(--red);background:var(--card)}
.cal{display:grid;grid-template-columns:repeat(7,1fr);gap:4px;margin:8px 0}
.cal button{aspect-ratio:1;background:var(--card);border:1px solid var(--line);color:var(--mut);font:700 13px Cairo,sans-serif;cursor:pointer;position:relative;padding:0}
.cal button.done{background:#000 var(--star) center/70% no-repeat;color:transparent}
.cal button.today{border:2px solid var(--red);color:var(--ink)}
.calh{display:grid;grid-template-columns:repeat(7,1fr);gap:4px;text-align:center;font:700 11px Cairo,sans-serif;color:var(--mut)}
.btn{font-weight:700;font-size:14px;color:var(--ink);background:none;border:1px solid var(--rule);padding:3px 14px;cursor:pointer;text-decoration:none;display:inline-flex;align-items:center;gap:6px}
.btn.run{background:var(--red);border-color:var(--red)}
.vn{width:18px;height:18px;border-radius:50%}.run .vn{animation:spin 1.6s linear infinite}@keyframes spin{to{transform:rotate(360deg)}}
.chips{display:flex;gap:6px;overflow-x:auto;margin-bottom:12px}
.chips button{flex:none;font:400 22px Anton,Impact,sans-serif;width:48px;height:48px;background:none;color:var(--mut);border:1px solid var(--line);cursor:pointer;position:relative}
.chips button.on{color:var(--ink);border-color:var(--red);background:#dcdad2}
.chips button.ok::after{content:"";position:absolute;top:3px;left:3px;width:12px;height:12px;background:var(--star) center/cover}
.num{font:400 clamp(4rem,18vw,7rem)/.9 Anton,Impact,sans-serif;color:var(--red);direction:ltr;text-align:right}
.tip{border-right:3px solid var(--amber);padding:2px 12px;margin:8px 0;color:#2a2a2a}.tip b{color:var(--amber)}.tip a,.t a{color:var(--amber)}
.dw{border-top:1px solid var(--rule)}.dw:last-child{border-bottom:1px solid var(--rule)}
.day{display:grid;grid-template-columns:78px 1fr auto 44px;gap:10px;align-items:center;padding:10px 2px}
.day.done{background:rgba(184,53,44,.10)}
.day .n{font:900 1.05rem Cairo,sans-serif;color:var(--red)}
.day .t{font-weight:700;line-height:1.4}.day .t small{display:block;color:var(--mut);font-weight:400;font-size:.85rem}
.m{font:700 12px Cairo,sans-serif;color:var(--amber);white-space:nowrap}
.acts{display:flex;flex-wrap:wrap;gap:6px;margin-top:6px}.acts .btn{font-size:12px;padding:1px 10px}
.chk{appearance:none;-webkit-appearance:none;width:38px;height:38px;border:2px solid #8a8880;background:var(--card);cursor:pointer;margin:0}
.chk:checked{border-color:var(--ink)}
.note{padding:0 2px 10px}.note textarea{width:100%;min-height:70px;background:var(--card);color:var(--ink);border:1px solid var(--line);padding:8px 10px;font:inherit;resize:vertical}
.cards h3{font-size:1.1rem;font-weight:900}.card{border-top:1px solid var(--rule);padding:10px 0}.card p{color:#2a2a2a}
.pics{display:grid;grid-template-columns:repeat(3,1fr);gap:8px;margin:8px 0 12px}.pics img{width:100%;aspect-ratio:1;object-fit:cover;border:1px solid var(--rule);padding:3px;background:var(--card)}
.slots{display:grid;grid-template-columns:repeat(auto-fill,minmax(150px,1fr));gap:8px;margin-top:12px}
.slot{position:relative;aspect-ratio:1;border:1px solid var(--rule);background:var(--card);overflow:hidden}
.slot img{width:100%;height:100%;object-fit:cover;display:block}.slot .ph{height:100%;display:grid;place-items:center;font-size:40px;color:#8a8880}
.slot label{position:absolute;inset:0;display:flex;align-items:flex-end;padding:6px 8px;font:700 13px Cairo,sans-serif;background:linear-gradient(transparent 60%,rgba(0,0,0,.8));cursor:pointer}.slot input{display:none}
.slot .x{position:absolute;top:5px;left:5px;z-index:3;width:28px;height:28px;border:0;background:rgba(0,0,0,.75);color:#fff;font-size:18px;cursor:pointer}
.cmp{position:relative;direction:ltr;aspect-ratio:1;max-width:540px;margin:0 auto;border:1px solid var(--rule);background:#000;overflow:hidden;--p:50%}
.cmp img{position:absolute;inset:0;width:100%;height:100%;object-fit:contain}.cmp .top{clip-path:inset(0 0 0 var(--p))}.cmp input{position:absolute;left:4%;width:92%;bottom:10px;z-index:3}
.cap{text-align:center;color:var(--mut);font-size:.9rem;margin-top:6px}
.gal{columns:2 150px;column-gap:8px}.gal img{width:100%;display:block;margin-bottom:8px;border:1px solid var(--rule);padding:3px;background:var(--card)}
.boom{position:fixed;top:-30px;width:26px;height:26px;border-radius:4px;z-index:50;animation:fall 1.7s ease-in forwards;pointer-events:none}
@keyframes fall{to{transform:translateY(112vh) rotate(360deg);opacity:.3}}
body::before{background:url("data:image/svg+xml;utf8,%3Csvg xmlns='http://www.w3.org/2000/svg' width='160' height='160'%3E%3Cfilter id='n'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='.8' numOctaves='2'/%3E%3CfeColorMatrix values='0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 .55 0'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23n)'/%3E%3C/svg%3E");opacity:.10}body::after{display:none}.slot label{color:#fff}details.st{padding:0 2px 10px}details.st summary{cursor:pointer;font:700 14px Cairo,sans-serif;color:var(--red)}details.st ol{padding-right:22px;margin:6px 0}details.st li{margin:2px 0}details.st p{color:#3a3a38}
.foot{text-align:center;color:var(--mut);font-size:.8rem;margin-top:24px;border-top:4px double var(--rule);padding-top:8px}
@media(max-width:560px){.day{grid-template-columns:1fr 44px;grid-template-areas:"n c" "t c" "m c"}.day .n{grid-area:n}.day .t{grid-area:t}.day .m{grid-area:m}.chk{grid-area:c}}
</style></head><body>
<div class="paper">
<div class="strip"><span>العدد الأول • السنة الأولى</span><span id="date"></span><span>ستة أسابيع</span></div>
<div class="mast"><img id="m1" alt=""><h1>التأسيس</h1><img id="m2" alt=""></div>
<nav><div id="tabs"></div></nav>
<section id="front">
 <div class="kick">الصفحة الأولى • نسخة الليل</div>
 <div class="hl">ست أسابيع من الصفر لين تمسكين الأدوات</div>
 <p class="dek">تتعلمين إيبس باينت خطوة خطوة بالآيباد والقلم اللي عندك. وبعدها نبدأ موقع الشهرين.</p>
 <figure><img id="lead" alt=""><figcaption>مرجع الأسلوب: ظل ورق قديم وخط يد. الصفحة الأولى، العدد الأول.</figcaption></figure>
 <div class="dbl"></div>
 <div class="kick" id="cdk">على نهاية التأسيس</div>
 <div class="cd" id="cd"></div>
 <div class="bar"><i id="fill"></i></div><div class="cap" id="count"></div>
 <div class="stars" id="stars"></div>
 <div class="dbl"></div>
 <div class="form"><div class="hl" style="font-size:1.3rem" id="fq"></div><div class="yn"><button id="yes"><img id="yimg" alt="">نعم</button><button id="no"><span class="x">×</span>لا</button></div><div class="cap" id="fmsg"></div></div>
 <div class="kick">التقويم • <span id="streakt"></span></div>
 <div class="calh" id="calh"></div><div class="cal" id="cal"></div>
 <div class="dbl"></div>
 <div class="kick">تحدي اليوم</div><button class="btn" id="chal">اعطيني فكرة</button><p class="dek" id="chalt"></p>
 <figure><img id="car" alt=""><figcaption>الأحمر والليل والمطر. هذا مزاج الموقع.</figcaption></figure>
</section>
<section id="weeks"><div class="chips" id="chips"></div><div id="wk"></div></section>
<section id="art"><div class="kick">رسوماتي</div><figure><img id="eyes" alt=""><figcaption>العين أصعب جزء، وأحلى واحد.</figcaption></figure><div id="artbox"></div></section>
<section id="dict"><div class="pics" id="s-dict"></div><div class="cards" id="c-dict"></div></section>
<section id="setup"><div class="pics" id="s-setup"></div><div class="cards" id="c-setup"></div></section>
<section id="gal"><div class="gal" id="g"></div></section>
<p class="foot">أسماء الأدوات قد تختلف قليلًا بين تحديثات التطبيق.</p>
</div>
<script>
var IMGS={"ball": "ball.jpg", "bat": "bat.jpg", "batlogo": "batlogo.jpg", "corvette": "corvette.jpg", "cowboy": "cowboy.jpg", "eyes": "eyes.jpg", "ferrari": "ferrari.jpg", "flame": "flame.jpg", "lead": "lead.jpg", "legs": "legs.jpg", "man": "man.jpg", "skull": "skull.jpg", "sniper": "sniper.jpg", "star": "star.jpg", "star_s": "star_s.jpg", "start": "start.jpg", "thebatman": "thebatman.jpg", "vinyl": "vinyl.jpg", "vinyl_s": "vinyl_s.jpg"};
var D={"weeks": [{"t": "تعرفين التطبيق والقلم", "m": 1, "i": "start", "w": "قناة ibis Paint الرسمية ← دروس البداية", "x": "تفتحين إيبس باينت وترسمين وتحفظين بدون ارتباك", "d": [{"n": "الأحد", "a": "قلمك والآيباد", "b": "تمرين: اكتبي اسمك بالقلم بثلاث أحجام", "c": "١٠", "q": "ibis paint x palm rejection stylus", "s": ["افتحي إيبس باينت وأنشئي ورقة جديدة (New Canvas).", "ارسمي بقلمك ثم بإصبعك وشوفي الفرق.", "ارجعي (Back) وافتحي الإعدادات (Settings) وشوفي خيار Palm Rejection. الخيارات تعتمد على نوع القلم، وقلم عادي غالبًا ما يظهر لك غير None."], "e": "كفك يرسم خطوط وانتي ترسمين. حطي ورقة أو منديل تحت كفك."}, {"n": "الاثنين", "a": "الورقة وحجمها", "b": "تمرين: ثلاث أوراق بأحجام مختلفة، ودائرة بكل وحدة", "c": "١٠", "q": "ibis paint x new canvas size", "s": ["من New Canvas جربي أحجام مختلفة، وابدئي بمربع كبير.", "كبّري الورقة وصغّريها بإصبعين وحركيها.", "انتبهي ما تصغرين الدقة كثير."], "e": "ورقة صغيرة جدًا تتكسر تفاصيلها لما تكبرينها. ابدئي بحجم كبير."}, {"n": "الثلاثاء", "a": "الفرش", "b": "تمرين: خط بخمس سماكات بفرشة وحدة", "c": "١٥", "q": "ibis paint x brush tool tutorial", "s": ["افتحي نافذة الأدوات واختاري الفرشاة (Brush).", "جربي ثلاثة أنواع من الفرش على الأقل.", "غيري الحجم والشفافية من الأشرطة."], "e": "تغيرين الفرشة كل دقيقة. ثبتي فرشة وحدة للتمارين."}, {"n": "الأربعاء", "a": "التراجع والمسح", "b": "تمرين: خمس شخابيط، وتراجعي عنها وحدة وحدة", "c": "١٠", "q": "ibis paint x undo redo eraser", "s": ["جربي أزرار التراجع والإعادة (Undo/Redo).", "اختاري الممحاة (Eraser) وجربي أحجامها.", "ابحثي إذا كانت ضغطة الإصبعين للتراجع مفعلة بنسختك."], "e": "تمسحين كل شي وتبدين من جديد. تراجعي خطوات أو امسحي الجزء بس."}, {"n": "الخميس", "a": "الألوان والقطّارة", "b": "تمرين: خمس دوائر بخمس ألوان تختارينها", "c": "١٥", "q": "ibis paint x quick eyedropper color window", "s": ["افتحي نافذة الألوان (Color window) واختاري لون.", "جربي القطّارة السريعة (Quick Eyedropper) لأخذ لون من الرسمة.", "وقت بدء القطّارة ينضبط من الإعدادات."], "e": "تضغطين وتسحبين فيرسم بدل ما يختار لون. ثبتي الضغطة ثواني."}, {"n": "الجمعة", "a": "الحفظ والتصدير", "b": "تمرين: صدّري رسمتك وارفعيها بتبويب رسوماتي", "c": "١٠", "q": "ibis paint x save image export", "s": ["ارجعي لمعرضك (My Gallery) وتأكدي إن رسمتك محفوظة.", "جربي حفظها كصورة من قائمة الحفظ والتصدير.", "احفظي نسخة بالصور عندك."], "e": "تمسحين التطبيق وتروح الرسمات. صدّري نسخة صورة دايمًا."}, {"n": "السبت", "a": "رسمة حرة", "b": "تمرين: عشر دقايق شخابيط بدون هدف", "c": "١٥", "q": "ibis paint x beginner drawing", "s": ["ورقة جديدة وفرشة وحدة.", "ارسمي ١٠ دقايق بدون ما تحكمين على رسمتك.", "احفظيها وصدريها."], "e": "تحكمين على رسمتك قبل ما تخلص. هذا أسبوع تعلم مو أسبوع تقييم."}]}, {"t": "الطبقات", "m": 1, "i": "ball", "w": "قناة ibis Paint الرسمية ← Layers", "x": "تفهمين الطبقات وتستخدمين Alpha Lock وClipping", "d": [{"n": "الأحد", "a": "إيش هي الطبقة", "b": "تمرين: وجه: طبقة للوجه وطبقة للشعر", "c": "١٥", "q": "ibis paint x layers for beginners", "s": ["افتحي نافذة الطبقات (Layer window).", "ارسمي دائرة بطبقة، وأضيفي طبقة جديدة وارسمي مربع.", "اخفي الطبقة الأولى وأظهريها بأيقونة العين."], "e": "ترسمين كل شي بطبقة وحدة. كل جزء بطبقته."}, {"n": "الاثنين", "a": "ترتيب الطبقات", "b": "تمرين: ثلاث دوائر متداخلة، وبدلي ترتيبها", "c": "١٠", "q": "ibis paint x reorder layers", "s": ["اسحبي الطبقات لتغيير ترتيبها.", "شوفي كيف الطبقة اللي فوق تغطي اللي تحتها.", "حركي طبقة بأداة التحويل."], "e": "ترسمين على الطبقة الغلط. تأكدي من الطبقة المحددة قبل الرسم."}, {"n": "الثلاثاء", "a": "الشفافية", "b": "تمرين: مسودة وردة بشفافية قليلة وخطوط فوقها", "c": "١٠", "q": "ibis paint x layer opacity", "s": ["اختاري طبقة وغيري شفافيتها (Opacity).", "خلي طبقة المسودة بشفافية قليلة.", "ارسمي فوقها طبقة خطوط."], "e": "المسودة تزعج الخطوط. خففي شفافيتها."}, {"n": "الأربعاء", "a": "التسمية والقفل", "b": "تمرين: سمي طبقات رسمة سابقة", "c": "١٠", "q": "ibis paint x name layers layer lock", "s": ["سمي طبقاتك (مثل: خطوط، لون، ظل).", "ابحثي عن قفل الطبقة (Layer Lock) بقائمة ⋮ في نافذة الطبقات إن كان موجود بنسختك.", "انسخي طبقة واحذفي أخرى."], "e": "طبقات اسمها Layer 1 إلى 12 وما تعرفين وش هي. سميها."}, {"n": "الخميس", "a": "التلوين تحت الخطوط", "b": "تمرين: لوني شكل بسيط تحت خطوطه", "c": "١٥", "q": "ibis paint x color fill undercoat", "s": ["طبقة للخطوط، وطبقة جديدة تحتها للون.", "استخدمي التعبئة (Color Fill) لتلوين الأساس.", "جربي التلوين بالفرشة بدل التعبئة."], "e": "التعبئة تترك فراغات حول الخط. تأكدي إن الخطوط مقفولة."}, {"n": "الجمعة", "a": "قفل الشفافية Alpha Lock", "b": "تمرين: غيري لون شكل بثلاث ألوان بدون ما تطلعين", "c": "١٥", "q": "ibis paint x alpha lock", "s": ["ارسمي شكل ملون على طبقة.", "فعلي Alpha Lock للطبقة.", "لوني بلون ثاني، وبيتلون داخل الشكل بس."], "e": "Alpha Lock ما يشتغل: لو الطبقة Vector حوليها لطبقة عادية. وما يشتغل على المجلدات."}, {"n": "السبت", "a": "القص Clipping", "b": "تمرين: كرة بلون وظل بطبقة Clipping", "c": "٢٠", "q": "ibis paint x clipping mask", "s": ["طبقة اللون، وفوقها طبقة جديدة للظل.", "فعلي Clipping على طبقة الظل.", "ارسمي ظل وما يتعدى حدود اللون."], "e": "الظل ما انقص. تأكدي إن الطبقة اللي تحته فيها اللون."}]}, {"t": "الأدوات المساعدة", "m": 1, "i": "man", "w": "قناة ibis Paint الرسمية ← Stabilizer وRulers", "x": "تتحكمين بالخط وتستخدمين المساطر والتحويل", "d": [{"n": "الأحد", "a": "Stabilizer", "b": "تمرين: عشرة خطوط طويلة بقيم مختلفة", "c": "١٥", "q": "ibis paint x stabilizer", "s": ["ابحثي عن إعداد Stabilizer بإعدادات الفرشة أو شريطها، ومكانه يختلف بنسختك.", "ارسمي خط بقيمة صفر، ثم متوسطة، ثم عالية.", "اختاري القيمة اللي تريحك."], "e": "القيمة العالية جدًا تخلي الخط يتأخر عن قلمك."}, {"n": "الاثنين", "a": "المساطر", "b": "تمرين: مربع ودائرة بالمسطرة", "c": "١٥", "q": "ibis paint x ruler tool", "s": ["افتحي أداة المسطرة (Ruler).", "جربي المسطرة المستقيمة والدائرية.", "ارسمي بمحاذاة المسطرة."], "e": "المسطرة تبقى مفعلة وانتي ما تحتاجينها. طفيها."}, {"n": "الثلاثاء", "a": "مسطرة التناظر", "b": "تمرين: فراشة بمسطرة التناظر", "c": "١٥", "q": "ibis paint x symmetry ruler", "s": ["جربي مسطرة التناظر (Symmetry ruler).", "ارسمي نص وجه وبيطلع الباقي.", "طفيها وكملي بدونها."], "e": "تعتمدين عليها بكل شي. استخدميها للتدريب."}, {"n": "الأربعاء", "a": "التحويل والتحريك", "b": "تمرين: وجه تحركينه وتكبرينه", "c": "١٥", "q": "ibis paint x transform tool", "s": ["اختاري طبقة وأداة التحويل (Transform).", "كبري وحركي ودوري.", "اقلبي الطبقة أفقيًا."], "e": "تحركين الطبقة الغلط. تأكدي من الطبقة المحددة."}, {"n": "الخميس", "a": "القلب لكشف الأخطاء", "b": "تمرين: وجه تقلبينه وتصححين ثلاث أخطاء", "c": "١٠", "q": "ibis paint x reflect horizontally", "s": ["ارسمي شي بسيط.", "اقلبيه أفقيًا.", "شوفي الأخطاء وصلحيها."], "e": "تصححين بدون ما تقلبين. القلب يوريك اللي ما شفتيه."}, {"n": "الجمعة", "a": "التحديد", "b": "تمرين: دائرة تحددينها وتلونين داخلها", "c": "١٥", "q": "ibis paint x selection tool", "s": ["جربي أداة التحديد (Selection).", "حددي جزء من الرسمة.", "انقليه أو امسحيه أو لونيه."], "e": "تنسين تلغين التحديد. ألغيه قبل ما ترسمين."}, {"n": "السبت", "a": "الصور المرجعية", "b": "تمرين: كوب من مرجع", "c": "١٥", "q": "ibis paint x display reference image", "s": ["ابحثي عن ميزة عرض صورة مرجعية (Display images to use as reference).", "حطي الصورة جنب رسمتك.", "ارسمي منها."], "e": "تنسخين الصورة نسخ. ابنيها بأشكالك."}]}, {"t": "الفرش والألوان", "m": 1, "i": "flame", "w": "قناة ibis Paint الرسمية ← Brushes وColor", "x": "تعرفين تختارين الفرشة واللون وتسوين تدرج", "d": [{"n": "الأحد", "a": "فرشة للمسودة وفرشة للخطوط", "b": "تمرين: نفس الشكل بفرشتين", "c": "١٥", "q": "ibis paint x best brushes for lineart", "s": ["اختاري فرشة قلم رصاص للمسودة.", "ابحثي عن فرشة حبر للخطوط النظيفة.", "ارسمي نفس الشكل بالفرشتين وقارني."], "e": "تجربين فرش كثيرة وما تتعلمين وحدة. اثنتين تكفي."}, {"n": "الاثنين", "a": "إعدادات الفرشة", "b": "تمرين: فرشة بحجم أدنى وشفافية تناسبك", "c": "١٥", "q": "ibis paint x brush settings", "s": ["افتحي إعدادات الفرشة.", "غيري الحجم الأدنى والشفافية.", "ابحثي عن قفل الفرشة (Brush Lock) إن كان بنسختك."], "e": "تعدلين الإعدادات وتنسين القيم القديمة. سجليها."}, {"n": "الثلاثاء", "a": "دائرة الألوان", "b": "تمرين: لونين متناسقين بدوائر", "c": "١٥", "q": "color theory basics for beginners", "s": ["افتحي نافذة الألوان.", "افهمي الفرق بين اللون والتشبع والإضاءة.", "اختاري لونين متناسقين."], "e": "ألوان صارخة كلها. خلي لون واحد هو الأقوى."}, {"n": "الأربعاء", "a": "لوحة ألوان", "b": "تمرين: شكل بسيط بلوحتك", "c": "١٥", "q": "ibis paint x color palette", "s": ["اجمعي خمس ألوان تحبينها، وممكن من ألوان صورك.", "ابحثي عن طريقة حفظ الألوان بنافذة الألوان.", "لوني شكل بها."], "e": "تختارين لون جديد كل مرة. اللوحة تريحك."}, {"n": "الخميس", "a": "التدرج", "b": "تمرين: ظللي كرة بالتدرج", "c": "٢٠", "q": "ibis paint x gradation shading", "s": ["ابحثي عن درس Making a Gradation في دروس إيبس باينت.", "جربي تدرج بين لونين.", "ظللي كرة بالتدرج."], "e": "التدرج يطلع بقع. ارسمي بضغطات خفيفة وكرريها."}, {"n": "الجمعة", "a": "الإضاءة والظل", "b": "تمرين: كرة حمراء تحت لمبة", "c": "٢٠", "q": "light and shadow basics digital painting", "s": ["اختاري مصدر ضوء.", "ظللي الجهة المعاكسة.", "أضيفي لمعة صغيرة."], "e": "الظل يجي من كل الجهات. حددي اتجاه ضوء واحد."}, {"n": "السبت", "a": "رسمة بثلاث ألوان", "b": "تمرين: أي شي ترسمينه بثلاث ألوان بس", "c": "٢٠", "q": "limited color palette drawing", "s": ["اختاري ثلاث ألوان من لوحتك.", "ارسمي شكل واحد بها.", "لا تزيدين لون رابع."], "e": "تزيدين ألوان لأنها متاحة. القيد يعلمك."}]}, {"t": "أول رسمة كاملة", "m": 1, "i": "cowboy", "w": "قناة ibis Paint الرسمية ← Drawing process", "x": "رسمة صغيرة كاملة من المسودة للتصدير", "d": [{"n": "الأحد", "a": "المسودة", "b": "تمرين: مسودة شكل بسيط تحبينه", "c": "٢٠", "q": "ibis paint x sketch draft layer", "s": ["ورقة جديدة وطبقة مسودة بشفافية قليلة.", "ارسمي شكل بسيط: كوب أو نجمة أو وردة.", "لا تهتمين بالنظافة."], "e": "تنظفين المسودة. المسودة للفوضى."}, {"n": "الاثنين", "a": "الخطوط النظيفة", "b": "تمرين: خطوط نظيفة فوق مسودتك", "c": "٢٠", "q": "ibis paint x clean lineart", "s": ["طبقة جديدة فوق المسودة.", "فعلي Stabilizer وارسمي الخطوط.", "اخفي المسودة وشوفي النتيجة."], "e": "تحاولين خط مثالي. خطوط مرتبة تكفي."}, {"n": "الثلاثاء", "a": "اللون الأساسي", "b": "تمرين: لوني تحت الخطوط", "c": "٢٥", "q": "ibis paint x coloring under lineart", "s": ["طبقة تحت الخطوط للون.", "استخدمي التعبئة أو الفرشة.", "اختاري ثلاث ألوان من لوحتك."], "e": "اللون يطلع برا الخطوط. كبري الورقة وصلحي الحواف."}, {"n": "الأربعاء", "a": "الظل", "b": "تمرين: ظل بطبقة Clipping", "c": "٢٥", "q": "ibis paint x shading clipping", "s": ["طبقة ظل فوق اللون وفعلي Clipping.", "حددي اتجاه الضوء.", "ظللي بفرشة ناعمة."], "e": "الظل ثقيل. خفضي شفافية الطبقة."}, {"n": "الخميس", "a": "اللمسات الأخيرة", "b": "تمرين: لمعة وخلفية بسيطة", "c": "٢٠", "q": "ibis paint x highlight background", "s": ["أضيفي لمعة صغيرة بطبقة جديدة.", "غيري لون الخلفية.", "قارني قبل وبعد."], "e": "تزيدين تفاصيل لين تخرب الرسمة. اوقفي قبل ما تتعبين."}, {"n": "الجمعة", "a": "التصدير", "b": "تمرين: صدري واعرضيها بتبويب رسوماتي", "c": "١٥", "q": "ibis paint x export image", "s": ["صدري الرسمة كصورة.", "ارفعيها بتبويب رسوماتي.", "اكتبي ملاحظة: وش الجزء اللي أتعبك."], "e": "تنسين الحفظ. صدري نسخة."}, {"n": "السبت", "a": "مراجعة", "b": "تمرين: رسمة صغيرة ثانية بنفس الخطوات", "c": "٢٠", "q": "ibis paint x drawing process", "s": ["اختاري شكل جديد.", "كرري الخطوات: مسودة، خطوط، لون، ظل.", "قارنيها بالأولى."], "e": "تقارنين رسمتك بفنانين محترفين. قارنيها برسمتك الأولى."}]}, {"t": "ثلاث رسمات صغيرة", "m": 1, "i": "legs", "w": "قناة ibis Paint الرسمية ← دروس الرسم", "x": "تثبتين كل شي بثلاث رسمات وتقارنين بأسبوعك الأول", "d": [{"n": "الأحد", "a": "رسمة ١: نجمة", "b": "تمرين: نجمة بخمس أطراف ببعد وظل", "c": "٢٠", "q": "ibis paint x draw star shading", "s": ["ارسمي نجمة بمسطرة أو بيدك.", "لوني وظللي بـ Clipping.", "صدريها."], "e": "الأطراف غير متساوية. اقلبي الرسمة وصححي."}, {"n": "الاثنين", "a": "رسمة ١: تحسين", "b": "تمرين: أضيفي خلفية وإضاءة", "c": "٢٠", "q": "ibis paint x background gradient", "s": ["أضيفي خلفية بتدرج.", "أضيفي لمعة.", "اكتبي ملاحظتك."], "e": "تغيرين اللي نجح. غيري اللي ما عجبك بس."}, {"n": "الثلاثاء", "a": "رسمة ٢: كوب", "b": "تمرين: كوب بقهوة وبخار من مرجع", "c": "٢٥", "q": "ibis paint x draw cup reference", "s": ["اعرضي صورة مرجعية لكوب.", "مسودة، خطوط، لون.", "ظللي بـ Clipping."], "e": "النسب غلط. اقلبي الرسمة أفقيًا."}, {"n": "الأربعاء", "a": "رسمة ٢: تحسين", "b": "تمرين: لمعة وانعكاس وظل على الطاولة", "c": "٢٠", "q": "ibis paint x shadow on table", "s": ["أضيفي ظل الكوب على الطاولة.", "لمعة صغيرة على الحافة.", "صدريها."], "e": "الظل بنفس لون الخلفية. خليه أغمق شوي."}, {"n": "الخميس", "a": "رسمة ٣: وجه بسيط", "b": "تمرين: وجه بسيط من مرجع بدون تفاصيل", "c": "٢٥", "q": "ibis paint x draw simple face", "s": ["اعرضي مرجع وجه بسيط.", "مسودة بدائرة وخطوط إرشاد.", "خطوط ثم لون أساسي."], "e": "تدخلين التفاصيل بدري. ابدئي بالشكل العام."}, {"n": "الجمعة", "a": "رسمة ٣: تحسين", "b": "تمرين: ظل وإضاءة على الوجه", "c": "٢٥", "q": "ibis paint x face shading", "s": ["ظللي بـ Clipping.", "لمعة صغيرة بالعين.", "صدريها."], "e": "الوجه مسطح. حددي اتجاه ضوء."}, {"n": "السبت", "a": "المراجعة", "b": "تمرين: قارني رسمتك الأولى بآخر رسمة", "c": "٢٠", "q": "ibis paint x progress comparison", "s": ["افتحي تبويب رسوماتي وقارني الأولى بالأخيرة.", "اكتبي ثلاث أشياء تعلمتيها.", "جاهزة لموقع الشهرين."], "e": "تشوفين الأخطاء بس. شوفي التقدم أول."}]}], "dict": [["Layer (طبقة)", "ورقة شفافة فوق ورقة. كل جزء من الرسمة ممكن يكون بطبقة."], ["Opacity (الشفافية)", "كم الطبقة ظاهرة. 100% كاملة، و30% باهتة."], ["Clipping (القص)", "الطبقة تظهر فقط داخل حدود الطبقة اللي تحتها."], ["Alpha Lock (قفل الشفافية)", "يخليك تلونين داخل الشكل فقط. ما يشتغل على طبقات Vector وطبقات المجلدات."], ["Stabilizer (المثبّت)", "يخلي الخط ناعم بتأخير بسيط بين قلمك والخط."], ["Ruler (المسطرة)", "تساعدك ترسمين خطوط مستقيمة ودوائر وتناظر."], ["Symmetry ruler", "مسطرة تناظر: ترسمين جهة وتنعكس الثانية."], ["Transform (التحويل)", "تكبير وتحريك وتدوير وقلب الطبقة."], ["Selection (التحديد)", "تحديد جزء من الرسمة للعمل عليه لحاله."], ["Color Fill (التعبئة)", "تعبئة منطقة بلون بضغطة."], ["Quick Eyedropper (القطّارة السريعة)", "ضغطة مطولة على لون بالرسمة لأخذه."], ["Undo / Redo", "تراجع وإعادة خطوة."], ["Eraser (الممحاة)", "تمسح من الطبقة المحددة بس."], ["Palm Rejection", "تجاهل لمسة الكف. الخيارات تعتمد على نوع القلم."], ["Brush Lock", "قفل إعدادات الفرشة (حسب نسختك)."], ["Layer Lock", "قفل طبقة عشان ما تتحرك أو تتعدل (من قائمة ⋮ بنافذة الطبقات حسب نسختك)."], ["Vector layer", "طبقة خطوطها قابلة للتعديل، لكن بعض الأدوات ما تشتغل عليها مثل Alpha Lock. حوليها لطبقة عادية."]], "setup": [["قلمك الرخيص", "الآيباد يتعامل معه مثل الإصبع، فما فيه حساسية ضغط. الخط بنفس السماكة، وتتحكمين فيها من حجم الفرشة."], ["كفك على الشاشة", "ممكن كفك يرسم خطوط. حطي ورقة أو منديل نظيف تحت كفك، أو قفاز رسم بدون أصابع. خيارات Palm Rejection بالإعدادات تعتمد على نوع القلم."], ["طرف القلم", "لو الطرف قاسي يخدش الشاشة أو الطرف مهترئ، لا تكملين فيه. الطرف يتبدل."], ["الإمساك والجلسة", "امسكي القلم بخفة، وارسمي بحركة الكتف للخطوط الطويلة. خذي استراحة كل 20 دقيقة."], ["متى أغير القلم؟", "مو الحين. ارسمي أسبوعين وشوفي وش يضايقك فعلًا، وبعدها نقارن لك خيارات حسب ميزانيتك."], ["لو ما لقيتي زر", "أسماء الأزرار ومواقعها تتغير بين نسخ إيبس باينت. ابحثي عن اسمه بالإنجليزي، أو افتحي دروس التطبيق الرسمية على ibispaint.com/lecture."]]};
var KEY="foundation-v1",KA="foundation-art",S={},A={};
try{S=JSON.parse(localStorage.getItem(KEY)||"{}")}catch(e){S={}}
try{A=JSON.parse(localStorage.getItem(KA)||"{}")}catch(e){A={}}
function save(){try{localStorage.setItem(KEY,JSON.stringify(S))}catch(e){}}
function saveA(){try{localStorage.setItem(KA,JSON.stringify(A));return true}catch(e){return false}}
function $(i){return document.getElementById(i)}
function esc(s){return String(s).replace(/&/g,"&amp;").replace(/</g,"&lt;").replace(/>/g,"&gt;")}
function mins(c){return +c.replace(/[٠-٩]/g,function(d){return "٠١٢٣٤٥٦٧٨٩".indexOf(d)})}
function ar(n){return String(n).replace(/\d/g,function(d){return "٠١٢٣٤٥٦٧٨٩"[d]})}
var st=document.createElement("style");st.textContent=":root{--star:url("+IMGS.star_s+")}.chk:checked{background:#000 url("+IMGS.star_s+") center/78% no-repeat}";document.head.appendChild(st);
[["m1","star_s"],["m2","star_s"],["lead","lead"],["car","ferrari"],["eyes","eyes"],["yimg","star_s"]].forEach(function(x){$(x[0]).src=IMGS[x[1]]});
var START=new Date(2026,10,15),END=new Date(2026,11,27);
$("date").textContent="السبت ١٤ نوفمبر ٢٠٢٦";
var T=[["front","الصفحة الأولى"],["weeks","الأسابيع"],["setup","قلمك والآيباد"],["dict","القاموس"],["art","رسوماتي"],["gal","المعرض"]];
$("tabs").innerHTML=T.map(function(t){return '<button data-t="'+t[0]+'">'+t[1]+'</button>'}).join("");
function show(id){if(!T.some(function(t){return t[0]==id}))id="front";
  document.querySelectorAll("section").forEach(function(s){s.classList.toggle("on",s.id==id)});
  document.querySelectorAll("nav button").forEach(function(b){b.classList.toggle("on",b.dataset.t==id)});
  if(location.hash!="#"+id)history.replaceState(null,"","#"+id);scrollTo(0,0)}
$("tabs").onclick=function(e){if(e.target.dataset.t)show(e.target.dataset.t)};
window.addEventListener("hashchange",function(){show(location.hash.slice(1))});
function card(id,arr){$(id).innerHTML=arr.map(function(a){return '<div class="card"><h3>'+a[0]+'</h3><p>'+a[1]+'</p></div>'}).join("")}
[["dict",["corvette","sniper","vinyl"]],["setup",["legs","skull","batlogo"]]].forEach(function(x){$("s-"+x[0]).innerHTML=x[1].map(function(n){return '<img src="'+IMGS[n]+'" alt="">'}).join("")});
card("c-dict",D.dict);card("c-setup",D.setup);
$("g").innerHTML=Object.keys(IMGS).filter(function(k){return !/_s$/.test(k)}).map(function(k){return '<img src="'+IMGS[k]+'" alt="" loading="lazy">'}).join("");
var cur=+(S.cur||0);
var P=["يد تمسك كوب","شخصية بقبعة وشال في يوم ممطر","وجه من ثلاث زوايا","سيارة تحت لمبة بالليل","عين فيها انعكاس الشارع","شعر يتحرك مع الهواء","حذاء وحوله طيات القماش","نفسك بعد خمس سنين","قطة نايمة بثلاث وضعيات","شخص من الخلف يطل من نافذة","كرة بلياردو بتظليل كامل","نجمة بخمس أطراف وثلاث ظلال","ظل شخص على جدار","يد تقلب صفحة","وجه ينظر للأعلى","ستيكر لشخصية تحبينها","جاكيت بطيات كثيرة","رجلين بحذاء رياضي","فنجان قهوة وبخار","رسمة سريعة بدقيقتين لأي شي حولك"];
$("chal").onclick=function(){$("chalt").textContent="ارسمي: "+P[Math.floor(Math.random()*P.length)]};
function dkey(d){return d.getFullYear()+"-"+(d.getMonth()+1)+"-"+d.getDate()}
function streak(){var n=0,d=new Date();S.dates=S.dates||{};if(!S.dates[dkey(d)])d.setDate(d.getDate()-1);while(S.dates[dkey(d)]){n++;d.setDate(d.getDate()-1)}return n}
function wkDone(i){return D.weeks[i].d.every(function(_,j){return S[i+"-"+j]})}
function todayIdx(){var t=new Date();t=new Date(t.getFullYear(),t.getMonth(),t.getDate());return Math.round((t-START)/864e5)}
var DN=["أحد","اثنين","ثلاثاء","أربعاء","خميس","جمعة","سبت"];
$("calh").innerHTML=DN.map(function(d){return "<span>"+d+"</span>"}).join("");
function drawCal(){var t=todayIdx();$("cal").innerHTML=Array.from({length:42},function(_,k){var i=Math.floor(k/7),j=k%7;return '<button data-k="'+k+'" class="'+(S[i+"-"+j]?"done ":"")+(k==t?"today":"")+'">'+ar(k+1)+'</button>'}).join("")}
$("cal").onclick=function(e){var k=e.target.dataset.k;if(k===undefined)return;cur=Math.floor(+k/7);S.cur=cur;save();draw();show("weeks")};
function update(){var n=0;D.weeks.forEach(function(w,i){w.d.forEach(function(_,j){if(S[i+"-"+j])n++})});
  $("count").textContent=ar(n)+" من ٤٢ يوم";$("fill").style.width=(n/42*100)+"%";$("streakt").textContent="أيام متتالية: "+ar(streak());
  $("stars").innerHTML=D.weeks.map(function(_,i){return '<img src="'+IMGS.star_s+'" class="'+(wkDone(i)?"on":"")+'" alt="">'}).join("");
  document.querySelectorAll(".chips button").forEach(function(b,i){b.classList.toggle("ok",wkDone(i))});
  document.querySelectorAll(".day").forEach(function(r,j){r.classList.toggle("done",!!S[cur+"-"+j])});drawCal();formUI()}
function formUI(){var t=todayIdx(),q=$("fq"),m=$("fmsg");$("yes").style.display=$("no").style.display=(t>=0&&t<42)?"":"none";
  if(t<0){q.textContent="يبدأ الأسبوع الأول يوم الأحد";m.textContent="";return}
  if(t>41){q.textContent="خلصتي التأسيس";m.textContent="";return}
  q.textContent="اليوم "+ar(t+1)+": هل رسمتي؟";m.textContent=S[Math.floor(t/7)+"-"+t%7]?"تم تسجيله. أحسنتي.":""}
function boom(){if(window.matchMedia&&matchMedia("(prefers-reduced-motion:reduce)").matches)return;
  for(var i=0;i<14;i++){var s=document.createElement("i");s.className="boom";s.style.background="url("+IMGS.star_s+") center/cover";s.style.left=Math.random()*94+"%";s.style.animationDelay=Math.random()*.5+"s";document.body.appendChild(s);setTimeout(function(x){return function(){x.remove()}}(s),2400)}}
function mark(i,j,v){var was=wkDone(i);S[i+"-"+j]=v;if(v){S.dates=S.dates||{};S.dates[dkey(new Date())]=1}save();
  var c=document.querySelector('.chk[data-j="'+j+'"]');if(c&&i==cur)c.checked=v;update();if(v&&!was&&wkDone(i))boom()}
$("yes").onclick=function(){var t=todayIdx();if(t>=0&&t<42)mark(Math.floor(t/7),t%7,true)};
$("no").onclick=function(){var t=todayIdx();if(t>=0&&t<42){mark(Math.floor(t/7),t%7,false);$("fmsg").textContent="ولا يهمك، بكرة يوم جديد."}};
function cdt(){var r=Math.max(0,END-new Date()),s=Math.floor(r/1000);
  $("cd").innerHTML=[[Math.floor(s/86400),"يوم"],[Math.floor(s%86400/3600),"ساعة"],[Math.floor(s%3600/60),"دقيقة"],[s%60,"ثانية"]].map(function(x){return "<div><b>"+x[0]+"</b><span>"+x[1]+"</span></div>"}).join("")}
cdt();setInterval(cdt,1000);
var tm=null;
function beep(){try{var c=new (window.AudioContext||window.webkitAudioContext)(),o=c.createOscillator(),g=c.createGain();o.connect(g);g.connect(c.destination);o.frequency.value=660;g.gain.value=.15;o.start();setTimeout(function(){o.stop();c.close()},700)}catch(e){}}
var TL='<img class="vn" src="'+IMGS.vinyl_s+'" alt="">';
function stopTimer(){if(tm){clearInterval(tm.id);if(tm.btn){tm.btn.innerHTML=TL+"ابدئي";tm.btn.classList.remove("run")}tm=null}}
function startTimer(btn,j,m){var same=tm&&tm.btn===btn;stopTimer();if(same)return;var end=Date.now()+m*60000,wi=cur;btn.classList.add("run");
  tm={btn:btn,id:setInterval(function(){var r=Math.max(0,Math.round((end-Date.now())/1000));btn.innerHTML=TL+Math.floor(r/60)+":"+("0"+r%60).slice(-2);
   if(r<=0){stopTimer();beep();try{navigator.vibrate&&navigator.vibrate([200,100,200])}catch(e){}mark(wi,j,true)}},250)}}
function draw(){stopTimer();var w=D.weeks[cur];
  $("chips").innerHTML=D.weeks.map(function(_,i){return '<button class="'+(i==cur?"on":"")+'" data-i="'+i+'">'+(i+1)+'</button>'}).join("");
  $("wk").innerHTML='<div class="kick">التأسيس • الأسبوع '+ar(cur+1)+' من ٦</div><div class="num">0'+(cur+1)+'</div><div class="hl">'+w.t+'</div>'
   +'<figure><img src="'+IMGS[w.i]+'" alt=""><figcaption>الأسبوع '+ar(cur+1)+': '+w.t+'</figcaption></figure>'
   +'<div class="tip"><b>شاهدي:</b> <a target="_blank" rel="noopener" href="https://www.youtube.com/results?search_query='+encodeURIComponent(w.w.replace(/[←•]/g," "))+'">'+w.w+'</a></div><div class="tip"><b>هدف الأسبوع:</b> '+w.x+'</div><div class="dbl"></div>'
   +w.d.map(function(d,j){var k=cur+"-"+j,nt=S["n"+k]||"";
    return '<div class="dw"><div class="day"><div class="n">'+d.n+'</div><div class="t">'+d.a+'<small>'+d.b+'</small><div class="acts"><button class="btn" data-act="timer" data-j="'+j+'" data-m="'+mins(d.c)+'">'+TL+'ابدئي</button><a class="btn" target="_blank" rel="noopener" href="https://www.youtube.com/results?search_query='+encodeURIComponent(d.q)+'">شاهدي الشرح</a><button class="btn" data-act="note" data-j="'+j+'">'+(nt?"ملاحظتي":"ملاحظة")+'</button></div></div><div class="m">'+d.c+' د</div><input type="checkbox" class="chk" data-j="'+j+'" aria-label="تم '+d.n+'"'+(S[k]?" checked":"")+'></div><details class="st"><summary>الخطوات</summary><ol>'+d.s.map(function(x){return "<li>"+x+"</li>"}).join("")+'</ol><p><b>غلطة شائعة:</b> '+d.e+'</p></details><div class="note"'+(nt?"":" hidden")+'><textarea data-nj="'+j+'" placeholder="وش صعب عليك اليوم؟ وش عجبك؟">'+esc(nt)+'</textarea></div></div>'}).join("");
  update()}
$("chips").onclick=function(e){if(e.target.dataset.i!==undefined){cur=+e.target.dataset.i;S.cur=cur;save();draw()}};
$("wk").onchange=function(e){if(e.target.classList.contains("chk"))mark(cur,+e.target.dataset.j,e.target.checked)};
$("wk").onclick=function(e){var b=e.target.closest("[data-act]");if(!b)return;var a=b.dataset.act;
  if(a=="timer")startTimer(b,+b.dataset.j,+b.dataset.m);
  if(a=="note"){var n=b.closest(".dw").querySelector(".note");n.hidden=!n.hidden;if(!n.hidden)n.querySelector("textarea").focus()}};
$("wk").oninput=function(e){if(e.target.dataset.nj!==undefined){S["n"+cur+"-"+e.target.dataset.nj]=e.target.value;save()}};
function drawArt(){var h=D.weeks.map(function(w,i){return '<div class="slot">'+(A[i]?'<img src="'+A[i]+'" alt=""><button class="x" data-del="'+i+'" aria-label="حذف">×</button>':'<div class="ph">+</div>')+'<label>الأسبوع '+ar(i+1)+'<input type="file" accept="image/*" data-up="'+i+'"></label></div>'}).join("");
  var ks=Object.keys(A).map(Number).sort(function(a,b){return a-b});
  var cmp=ks.length>1?'<div class="cmp" id="cmp"><img src="'+A[ks[0]]+'" alt=""><img class="top" src="'+A[ks[ks.length-1]]+'" alt=""><input type="range" min="0" max="100" value="50" id="rg" aria-label="مقارنة"></div><p class="cap">اسحبي المؤشر: الأسبوع '+ar(ks[0]+1)+' (يسار) والأسبوع '+ar(ks[ks.length-1]+1)+' (يمين)</p>':'<p class="cap">ارفعي رسمة من أسبوعين مختلفين لتظهر المقارنة. الرسمات تنحفظ على جهازك فقط.</p>';
  $("artbox").innerHTML=cmp+'<div class="slots">'+h+'</div>';
  var rg=$("rg");if(rg)rg.oninput=function(){$("cmp").style.setProperty("--p",rg.value+"%")}}
$("artbox").onchange=function(e){var i=e.target.dataset.up,f=e.target.files&&e.target.files[0];if(i===undefined||!f)return;
  var r=new FileReader();r.onload=function(){var im=new Image();im.onload=function(){var m=800,s=Math.min(1,m/Math.max(im.width,im.height)),c=document.createElement("canvas");c.width=Math.round(im.width*s);c.height=Math.round(im.height*s);c.getContext("2d").drawImage(im,0,0,c.width,c.height);
    var old=A[i];A[i]=c.toDataURL("image/jpeg",.78);if(!saveA()){if(old)A[i]=old;else delete A[i];alert("المساحة امتلأت، احذفي رسمة قديمة أولًا.")}drawArt()};im.src=r.result};r.readAsDataURL(f)};
$("artbox").onclick=function(e){if(e.target.dataset.del!==undefined){delete A[e.target.dataset.del];saveA();drawArt()}};
draw();drawArt();show(location.hash.slice(1));
</script>
</body></html>

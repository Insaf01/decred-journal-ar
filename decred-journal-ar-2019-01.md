
# صحيفة الديكريد لشهر يناير2019 

![abstract art](journal-201901-384.jpg)

شهد الديكريد بداية سنة 2019 إصدارات كبيرة للبرمجيات والتطورات الهامة في أجزاء أخرى من المشروع. 

تم [إصدار](https://github.com/decred/decred-binaries/releases/tag/v1.4.0) نسخة جديدة من برنامج العقدة والمحفظة (نسخة 1.4.0) والتي ستطلق التصويت على قواعد الإجماع (من بين أمور أخرى)،  لذا ننصح بتحديث نسختكم الحالية. 

تم إصدار محفظة الهاتف النقال لdcrandroid  والتي تستخدم آلية النظام البسيط للتحقق من الدفع نظير لنظير(نسخة 1.0) وأصبحت متاحة على [جوجل بلاي ستور](https://play.google.com/store/apps/details?id=com.decred.dcrandroid.mainnet).

تم [نشر](https://proposals.decred.org/proposals/5431da8ff4eda8cdbf8f4f2e08566ffa573464b97ef6d6bae78e749f27800d3a) اقتراح RFP للبنية الأساسية للتبادل اللامركزي والذي تم وصفه بواسطة jy-p@ في تدوينة سابقة على موقع على منصة بوليتيا. 

كما تم [الانتهاء](https://pastebin.com/E5L6u2RV) من عملية الاستشارة المجتمعية لتحديد الرسائل الأساسية للديكريد، ويتمثل الشعار المحدد  في هذه المراسلة :"الديكريد: آمن. قابل للتكيف. و ذاتي التمويل." وتحولت جهود التوعية إلى التخطيط لأنشطة السنة، مع مشاركة المقترحات المسبقة بشأن [الفعاليات](https://www.reddit.com/r/decred/comments/anhh8n/proposal_to_get_events_spending_approved_via/) والإنفاق [التسويقي](https://www.reddit.com/r/decred/comments/aolr79/politeia_proposal_to_fund_marketing_ops_for_2019/) على مواقع الدردشة و موقع "ريديت".

ويغطي هذا الإصدار أيضًا أحداث أوائل شهر فبراير، حيث حدثت عدة تطورات هامة، واعتبر من المفيد تضمينها قبل إصدار فبراير.

## تحديث النسخة 1.4.0 والتصويت على قواعد الإجماع

تم إصدار النسخة 1.4.0 لبرنامج العقدة والمحفظة. ملاحظات الإصدار والتنزيلات الكاملة أصبحت متوفرة على [GitHub](https://github.com/decred/decred-binaries/releases/tag/v1.4.0). قم بالتأكد دائمًا من [التحقق من التنزيلات](https://docs.decred.org/advanced/verifying-binaries/).

يوفر هذا الإصدار تحسينات مهمة، بالإضافة إلى تغيير مقترح قواعد الإجماع الذي يعمل على إصلاح الخلل بدعم شبكة البرق. وينصح مشغلي العقدة بتحديث نسخة البرنامج لمساعدة الشبكة في الوصول إلى الحد الأدنى للتحديث. وبمجرد ترقيته ، ينبغي للناخبين أن يضعوا [تفضيلات التصويت](https://docs.decred.org/governance/how-to-vote/). يمكن تتبع تقدم التحديث على [voting.decred.org](https://voting.decred.org/).

للحصول على التفاصيل التقنية لتغير قواعد الإجماع، انظر [DCP004](https://github.com/decred/dcps/blob/master/dcp-0004/dcp-0004.mediawiki) و [العمود](https://matheusd.com/post/dcp0004-and-hardforks/) المنشور  بواسطة matheusd@.
باستثناء جدول أعمال التصويت، لا تضم النسخة النهائية من الإصدار 1.4.1 على أي تغييرات مهمة أخرى منذ الإصدار 2 من المرشح الذي تم تغطيته في [دجنبر](https://xaur.github.io/decred-news/journal/201812.html).

## التطوير

[dcrd](https://github.com/decred/dcrd): تم إيجاد خطأ في [النسخة](https://github.com/decred/dcrd/issues/1568) 1.4.0 RC1. أدى التغيير الكبير الذي طرأ على نظام وضع الدلالات لنواتج المعاملات غير المنفقة UTXO set semantics إلى إصلاح بالخطأ علة كانت توجد في قواعد الإجماع. وقد تم [الحفاظ](https://github.com/decred/dcrd/pull/1570) على السلوك الخطأ القديم حتى يمكن إجراء تصويت بالإجماع لتصحيح ذلك. شكرا لكل من ساعد على اكتشاف وإصلاح العلة  في مرشح الإصدار.

[إكتمل](https://github.com/decred/dcrd/pull/1579) رمز التصويت لقواعد الإجماع وتم تضمينه في [الإصدار النهائي للنسخة 1.4.1](https://github.com/decred/decred-binaries/releases/tag/v1.4.0).  وقد أعطيت الأولوية للتصحيح والتصويت لأنه مطلوب من أجل شبكة البرق. [DCP004](https://github.com/decred/dcps/blob/master/dcp-0004/dcp-0004.mediawiki) (مقترح الديكريد للتغيير) يشرح  التغيير بالتفصيل ويذكر التطبيقات المفيدة للأقفال النسبية وراء شبكة البرق.   ومن الأثر الجانبي لهذا العمل، [إعادة تحليل](https://github.com/decred/dcrd/pull/1583) وتعزيز الاختبارات في ذلك المجال.  نشر matheusd@  [تدوينة](https://matheusd.com/post/dcp0004-and-hardforks/) تعطي لمحة عامة عن العلة وكيفية العثور عليها والرد عليها. 	

[بدأت](https://github.com/decred/dcrd/issues/1593) المناقشة في كيفية زيادة تحسين خوارزمية صعوبة المشاركة عن طريق إزالة التذبذبات -وهذا من شأنه أن يجعل سعر التذكرة أكثر سلاسة.

[Decrediton](https://github.com/decred/decrediton): إصلاح العلل والتحضير لإصدارالنسخة 1.4.0.
ميزة لتحديد خيارات التكوين حيث تم [دمج](https://github.com/decred/decrediton/pull/1975) وسيطات سطر الأوامر لإتقانها. 

[Politeia](https://github.com/decred/politeia): تم تمكين ميزة لعرض الإصدارات السابقة من الاقتراح.

في مجال التطوير: [استعيض ](https://github.com/decred/politeiagui/pull/986)عن برنامج "Onboarding popup" بروابط ذات صلة بالمستندات. شكرا لـ lemonkabir لإكتشافه بعض [المشاكل الأمنية](https://github.com/decred/politeia/issues/647). دخلت [طبقة الذاكرة المؤقتة](https://github.com/decred/politeia/pull/660) مرحلة المراجعة.

### مناقشات:

* تم تحديد [ميزة](https://github.com/decred/politeia/issues/662) المشرف المفقودة لفرض الرقابة على الاقتراح العام: يجب أن تكون هناك طريقة لإزالة اقتراح عام تم تعديله بحيث يشمل محتوى مسيء. وكبديل لذلك، سيتعين على المشرفين مراجعة جميع التعديلات قبل عرضها في موقع المقترحات.
* [الاختبار الأتوماتيكي من البداية إلى النهاية](https://github.com/decred/politeiagui/issues/976) و [قائمة الأسئلة والأجوبة](https://github.com/decred/politeiagui/issues/977) لإجراء تغييرات رئيسية.
* [إعادة تحليل](https://github.com/decred/politeiagui/issues/990) شفرة الواجهة الأمامية لمعالجة مشكلات التعقيد والأداء وإنتاجية المطورين. [الحل](https://github.com/decred/politeiagui/issues/990#issuecomment-454535696) المقترح الأول هو استخدام GraphQL.

[dcrandroid](https://github.com/decred/dcrandroid): تم إصدار النسخة النهائية 1.0! احصل عليها على متجر Google Play  لمحافظ [الشبكة الرئيسية](https://play.google.com/store/apps/details?id=com.decred.dcrandroid.mainnet) أو [الشبكة الإختبارية](https://play.google.com/store/apps/details?id=com.decred.dcrandroid.testnet). يمكنك الحصول على العملات الإختبارية عن طريق [الصنبور](https://faucet.decred.org/). جميع  تعليقاتكم مرحب بها على [Reddit](https://www.reddit.com/r/decred/comments/am7j40/decred_wallet_for_android_v10_released/)  وتقارير العلة [على GitHub](https://github.com/decred/dcrandroid/issues).
منذ إصدار المرشح 2، أضافت النسخة النهائية عرض تقدم المزامنة، عدم وجود منبه للإنترنت اللاسلكي، شاشة بداية جديدة  مع إصلاح طفيف للعلل - كامل سجلّ التغييرات [هنا](https://github.com/decred/dcrandroid/compare/v1.0.0-rc2...v1.0.0-rc3). تهانينا لفريق dcrandroid!

[dcrios](https://github.com/raedahgroup/dcrios):المعاينة [متاحة](https://testflight.apple.com/join/dvq51tCh) على Apple TestFlight.

[dcrdata](https://github.com/decred/dcrdata): تصميم الصفحة الرئيسية الجديدة في [تقدم](https://github.com/decred/dcrdata/pull/921). يتم الآن [التحديث التلقائي](https://github.com/decred/dcrdata/pull/961) للقيم على الصفحة الرئيسية عند العثور على كتلة جديدة. تمت [إضافة](https://github.com/decred/dcrdata/pull/951) مراقبة سعر الصرف إلى الواجهة الخلفية والتي تمكن من إظهار قيم الدولار الأمريكي على واجهة المستخدم. ويجري الآن إنفاذ نظام https على المستكشف و النطاقات الفرعية للشبكة الرئيسية  [نقاش](https://matrix.to/#/!MgQoetFiyjrHAywokv:decred.org/$154818146313660CWvZy:decred.org).

تصميم الصفحة الرئيسية الجديد الذي يتضمن سعر الصرف، عرض جدول عناوين جديد، مخططات محسنة، وتحسينات السرعة أصبح [متاحا](https://twitter.com/decredexplorer/status/1093182831487053825) في النسخة v4 beta على [beta.dcrdata.org](https://beta.dcrdata.org/). سيتم تجميع ملاحظات الإصدار التفصيلية مع مرشح الإصدار.

جانب التطوير: [يدمر](https://github.com/decred/dcrdata/pull/915) buck54321@ رمز jQuery الإلزامي. يقوم الفريق بإعداد اختبار الإجهاد لواجهة برمجة تطبيقات تبصرية _(يسمونه اختباراً للتعذيب ، أوش)_. 

[تقسيم التذاكر](https://github.com/matheusd/dcr-split-ticket-matcher): تحسينات في الشفرة الداخلية ، العمل التمهيدي لإدماج Decrediton. تم إعداد [صفحة مراقبة](https://mainnet-split-tickets.matheusd.com/) تعرض جلسات تقسيم نشطة من جميع مقدمي خدمة التصويت VSPs التي تدعمها.

[مستندات](https://github.com/decred/dcrdocs): صفحات جديدة: يعمل [مقدم خدمة التصويت](https://docs.decred.org/advanced/operating-a-vsp/) على تحديد متطلبات التكوين والمهارات المطلوبة لمشغلي خدمة التصويت، ويقدم  [التصويت المنفرد بإثبات العمل](https://docs.decred.org/advanced/solo-proof-of-stake-voting/) ل jz@  دليلا لجميع قارئي المستندات، كما تصف [تفاصيل العناوين](https://docs.decred.org/advanced/address-details/) جميع الأنواع المحتملة للعناوين، وتوضح [المساهمة في الديكريد](https://docs.decred.org/contributing/contributing-to-decred/) كيف تصبح مقاولا مدفوع الأجر.

استنتجت المناقشة الأمنية العميقة في documentation# أنه من الممكن تجميع [الإرشادات العامة لأمن الكمبيوتر](https://github.com/xaur/decred-issues/issues/101) والتي ستكون من شأنها أن تكون مفيدة في الفضاء بأكمله.

[decred.org](https://github.com/decred/dcrweb): تم [ضم](https://github.com/decred/dcrweb/pull/491) جهد ضخم لترحيل الموقع إلى Hugo بواسطة peter\_zen@. هوغوهو مولد موقع ثابت كتب في go والذي يجعل تحديث محتوى الموقع أسهل بكثير. تم تفعيل عدة عمليات [لتحسين](https://github.com/decred/dcrweb/pull/513) سرعة الموقع.  يتم [تحديث](https://github.com/decred/hardforkdemo/commits/master) لوحة الاقتراع في [voting.decred.org](https://voting.decred.org/) تمهيدا للتصويت على الإجماع القادم -  مبروك لjholdstock@ للتعمق في Go!

### مسائل أخرى:

* تم بناء الموقع الجديد [لمكافأة إيجاد العلة](https://bounty.decred.org/) أيضا بواسطة  Hugo.  [مستودع](https://github.com/decred/dcrbounty) الرموز مفتوح لتقارير الأخطاء والمساهمات.
* المزيد من تغييرات المصطلحات في  dcrwallet ، dcrdocs و dcrweb.
* تتحول المشاريع تدريجيا إلى golangci-lint linter  أكثر سرعة.
* تم [تمكين](https://github.com/decred/dcrweb/pull/537) المزيد من ترويسات الأمان على decred.org.
* قد تكون [واجهة SQL](https://www.reddit.com/r/decred/comments/agpkjv/sql_interface_to_live_onchain_decred_data/) الخاصة ببيانات السلسلة المفردة مثيرة للاهتمام للباحثين.
* يتيح [GitHub](https://github.blog/2019-01-07-new-year-new-github/) الآن للمستودعات الخاصة مع ما يصل إلى 3 متعاونين للحسابات المجانية.

إحصائيات نشاط التطوير لشهر يناير: 242 من المشاريع النشطة، 243  إلتزام، 60 ألف إضافة، 47 ألف عملية حذف  خلال  8 سجلات. وجاءت المساهمات من 2 إلى 8 مطورين لكل مستودع.

## الاشخاص:

مرحبا بالمساهمين الأوائل الجدد مع دمج الرمز على Github: 
- Sarlor في [dcrd](https://github.com/decred/dcrd/commits?author=Sarlor)
- lazlom في [decrediton](https://github.com/decred/decrediton/commits?author=laszlolm)
- dezryth في [dcrdocs](https://github.com/decred/dcrdocs/commits?author=dezryth)

تهانينا لستة من المساهمين الجدد الذين تم [إدراجهم](https://github.com/decred/dcrdocs/commits?author=dezryth) في decred.org:

* David Habibi @eSizeDave، مدبر المجتمع- أستراليا
* Elian Huesca @elian، مدبر المجتمع- المكسيك
* Marcelo Martins @mm، مدبر المجتمع-البرتغال
* Mariusz Szyma @donmario، مدبر المجتمع - بولاندا
* Morphy Tsai @morphymore، مدبر المجتمع - التايوان
* Tomasz Porwit @kozel ، التعليم والتواصل

تمت [إزالة](https://github.com/decred/dcrweb/issues/528) 4 مطورين غير نشطين من decred.org:
- Cruz Molina، الملقب بfreethinkingaway@ من dcrdata
- Huy Nguyen Tuan، الملقب بhuyntsgs@ من dcrwallet
- Macaulay Davies، الملقب بmcedward@ من Rohit Nagori.

وقد [نشر ](https://medium.com/decred/decred-independent-contractor-roadmap-884faba3db39)المقاولون المستقلون للديكريد خططهم لعام 2019 ، وذلك بفضل ~ مساهمة 15 شخص . وقد أثار هذا المقال [مناقشة](https://matrix.to/#/!OfChXgczrIlpEZSFAv:decred.org/$15476119656176jVTYW:decred.org) بشأن خرائط الطرق والتخطيط المركزي والاستقلال الذاتي للمتعاقدين ، فضلا عن تعليقات من منظمة "ديتو" (Ditto).

## الإدارة

في يناير، تلقت [الخزنة](https://explorer.dcrdata.org/address/Dcur2mcGjmENx4DhNqDctW5wJCVyT3Qeqkx) 16.776 وحدة نقدية للديكريد DCR، أنفقت منها 9.991 DCR.باستخدام المعدل اليومي  لشهر يناير من DCR / USD والذي يبلغ قدره 17,1 دولارًا ، سيكون لدينا مبلغ 286 ألف دولار أمريكي تم إستلامه و 170 ألف دولار أمريكي تم إنفاقه. وبما أن هذه المدفوعات كانت للعمل المنجز في شهر دجنبر، فإنه من المفيد أيضاً النظر فيها في سياق المعدل اليومي لمتوسط شهر دجنبر البالغ 17.5 دولار - وفي هذه الحالة فإن الأرقام التي تم تلقيها / إنفاقها بالدولار الأمريكي هي 294 ألف دولار / 175 ألف دولار.

المقاولون الآن [يتقاضون أجورهم](https://docs.decred.org/contributing/contributor-compensation/) في~15 من كل شهر عن عملهم الشهر خلال السابق.  التأخير بين الفوترة و الدفع تم خفضه إلى النصف من ~اليوم الثلاثين. والعمل جار لزيادة تخفيض هذا التأخير.

تم [تقديم](https://proposals.decred.org/proposals/5431da8ff4eda8cdbf8f4f2e08566ffa573464b97ef6d6bae78e749f27800d3a) اقتراح البنية التحتية اللامركزية للتبادل  للديكريد بواسطة jy-p@. فهو يحدد الحافز والتصميم العالي المستوى لDEX و الذي تم وصفه لأول مرة في  [عمود](https://blog.decred.org/2018/06/05/A-New-Kind-of-DEX/)  يونيو 2018. و من المتوقع أن يكتمل المشروع في أقل من 6 أشهر بميزانية تتراوح بين 100.000 و 1.000.000 دولار أمريكي. وسيجرى التصويت على مرحلتين: سيقرر المقترح الأول ما إذا كان أصحاب الحصص يريدون متابعة ذلك، وإذا ما تمت الموافقة على الاقتراح الأول، سيتم إستدعاء المقترحات من الفرق المهتمة، وستتمثل المرحلة الثانية في اختيار أحد هذه المقترحات. تُعرف هذه العملية باسم [طلب الاقتراح](https://en.wikipedia.org/wiki/Request_for_proposal).

تم [إطلاق](https://twitter.com/decredproject/status/1087486930093264897) برنامج مكافأة إيجاد العلة للديكريد في أعقاب [تصويت](https://proposals.decred.org/proposals/d33a2667469b56942adf42453def6cc2292325251e4cf791e806939ea9efc9e1) ناجح في دجنبر. تحقق من القواعد على الموقع الجديد[bounty.decred.org](https://bounty.decred.org/)  و مدونة المقدمة على [hackernoon](https://hackernoon.com/decred-launches-debug-decred-bug-bounty-program-7e4d2af27ec9). كل الشكر والتقدير ل fernandoabolafio@  و jholdstock@  لمعظم أعمالهم على الموقع. فريق المكافآت الذي يبث في صحة الطلبات والمدفوعات يشمل degeri@ وdnldd@ وfernandoabolafio@ وjholdstock@ وmatheusd@. مبروك للفريق على التدشين!

يقوم Dustorf@ بإعداد مقترحات لتحسين الشفافية وزيادة سيطرة أصحاب الحصص على تخصيص الأموال لأنشطة التسويق.  تم نشر [المقترح القبلي](https://www.reddit.com/r/decred/comments/anhh8n/proposal_to_get_events_spending_approved_via/) لنفقات الفعاليات على Reddit   لتلقي التعاليق بعد تكراره في [الدردشة](https://matrix.to/#/!aNPTuiryMFmdMQWUzb:decred.org/$154896889724431Mxlvj:decred.org).  كما بدأ في الدردشة المقترح القبلي لميزانية التسويق ليتم تنزيله على [Reddit ](https://www.reddit.com/r/decred/comments/aolr79/politeia_proposal_to_fund_marketing_ops_for_2019/) بعد الجولة الأولى من التعاليق.

oregonisaac@ [يبحث](https://matrix.to/#/!MIGqWXfLFBwhipPKYL:decred.org/$15474111512672Whvns:decred.org) عن مطوري جافا لتقييم متطلبات إدماج أجهزة الصراف الآلي. تم نشر مشروع الاقتراح ومناقشته في [الدردشة](https://matrix.to/#/!MIGqWXfLFBwhipPKYL:decred.org/$154828004015153jWdiD:decred.org). كان هناك بعض الإجماع على استخدام التصويت على RFP ( تقديم اقتراح البنية التحتية اللامركزية للتبادل  للديكريد)  على مرحلتين.  ومن النقاط الجيدة الأخرى التي نوقشت ما إذا كان ينبغي انتظار إطلاق تطبيقات الهاتف النقال قبل الشروع في أجهزة الصراف الآلي. 

### مناقشات:

* حفز اقتراح Baeond على [مناقشة](https://matrix.to/#/!MIGqWXfLFBwhipPKYL:decred.org/$15468733339790vCEoH:decred.org) قوة موجهة للهجوم حيث سيعرض على أصحاب الحصص أخذ بعض العملات الرمزية مقابل موافقتهم على الاقتراح. 
* [المشاركة](https://matrix.to/#/!MIGqWXfLFBwhipPKYL:decred.org/$15481365491827928DiBLm:matrix.org) والرضا مع بوليتيا لحد الآن.
* كيف يمكن [لتحسينات UX](https://github.com/decred/politeia/issues/678) مساعدة الناخبين على التعامل مع المقترحات السيئة بشكل استباقي والبقاء يقظين.

## شبكة الاتصال:

معدل الهاش: افتتحت معدلات الهاش شهر يناير في ~187 Ph/s وأغلقت عند ~225 Ph/s وبلغ قاعها 144 Ph/s وبلغت ذروتها 312 Ph/s على مدار الشهر. اعتبارا من 8 فبراير، بلغ توزيع مجمع معدل الهاش حسب [dcrstats.com](https://dcrstats.com/pow) :
- F2pool 26%
- BTC.com 19%
- UUPool 8%
- Luxor 4%
- CoinMine 1%
- أخرى 13%   

أرقام توزيع المجمع تقريبية ولا يمكن تحديدها بدقة.

تحصيص: كان متوسط سعر التذكرة لمدة 30 يومًا 109.4 (DCR (+6.4 في 4 فبراير حسب dcrstats.com. تفاوت السعر بين 101.5-111.6 DCR. المبلغ المقفل كان 4.20-4.38 مليون DCR،  وهو ما يعادل 46.3-47.5 ٪ من العرض المتاح.

كان هناك 90 تذكرة مجزأة في يناير. وتظهر [البيانات](https://gist.github.com/oregonisaac/8eb4d50af9fa888c920666fb73ba44b2) منذ ماي 2018 نموًا ثابتًا.

العقد:اعتبارا من 4 فبراير كان هناك 197 عقدة استماع عام و 369 عقدة عادية حسب [dcred.eu](https://dcred.eu/nodeStats). توزيع الإصدار: بناء التطوير النسخة 1.5.0: 4.3% (2.8%+)، بناء التطوير و إصدار الصيغة المرشحة النسخة 1.4.0: 13% (6%+)، النسخة 1.3.0: 55%، النسخة 1.2.0: 14% (-6%)، النسخة 1.1.2: 8% (-2%)، 1.1.0: 3% (-1%).

## تعدين

يتم [شحن](https://us16.campaign-archive.com/?u=393b2698d17bdfe48ac0422ac&id=4211e39081) Obelisk batches 2-5، [تحديثات](https://us16.campaign-archive.com/?u=393b2698d17bdfe48ac0422ac&id=c501bf724d) البرامج الثابتة ل Gen 2  تحتوي على ميزات جديدة مع إصلاح العلل.  تم رفع [دعوى جماعية](https://www.reddit.com/r/decred/comments/ae8hy8/class_action_lawsuit_officially_filed_against/) على بيع Obelisk من SC1 و DCR1.

المصدر المفتوح لإدماج مجمع التعدين [قيد التنفيذ](https://medium.com/decred/decred-independent-contractor-roadmap-884faba3db39) بواسطة dnldd@.

## عمليات الإدماج

إنضم مقدم خدمات التصويت الجديد [dcr.grassfed.network](https://dcr.grassfed.network/)  إلى قائمة تضم ما مجموعه 23 من مقدمي خدمات التصويت. 

### إدماج منصات التبادل:

* [أعلنت](https://twitter.com/bitturkcom/status/1082201314912862209) منصة التبادل التركية إضافة زوج عملة الفياتDCR/TRY،المناقشة وبعض المعلومات الأساسية [هنا](https://matrix.to/#/!OfChXgczrIlpEZSFAv:decred.org/$15468134682383442wwDSE:matrix.org).
* [أعلنت](https://twitter.com/bitjabr/status/1090066185302036480) منصة التبادل BitJa إضافة زوج عملة الفيات DCR/BRL.

[أعلنت](https://twitter.com/ellipalwallet/status/1089850526202613760) محفظة Ellipal دعم الديكريد في أحدث إصدار للبرامج الثابتة.

[أدمجت](https://twitter.com/exodus_io/status/1090263399122923520) محفظة Exodus USDC، رمزا مرتبطا بالدولار.

[ضمت](https://medium.com/@artikozel/decred-infrastructure-interviews-stephen-founder-of-crypto-only-luxury-goods-marketplace-68d3214a4fd7) الحلقة الثانية من سلسلة مقابلات البنية التحتية ل kozel@ ستيفن، مؤسس سوق تصريف السلع الكمالية Crypto Emperium. شارك ستيفن  وجهات نظره حول إدارة الأعمال، قبول العملات الرقمية، أوامر المعالجة، سلسلة الإمدادات، والخطط المستقبلية.

> منتجنا الأفضل مبيعًا على الموقع كان بلا شك [سترة الديكريد لجاك](https://www.cryptoemporium.eu/product/decred-jacket/) الشهيرة! لقد تشرفت بخدمة مجتمع الديكريد لفترة طويلة وساعدت في تسويق مشروع أؤمن به حقًا. 

قم دائمًا بالبحث _قبل_استخدام المحافظ أو الخدمات، خاصةً تلك التي تحتفظ بأموالك.

## اعتماد

[أعلنت](https://medium.com/@BlueYard/blueyard-2-3d0bbaf1f1b6) "بلو يارد" عن الحملة الثانية لجمع التبرعات وشرحت استراتيجيتها للاستثمار في المشاريع المتناقضة.

## مد الخدمة

[يعتزم](https://matrix.to/#/!OfChXgczrIlpEZSFAv:decred.org/$15468814029997AWtQJ:decred.org) فريق التسويق التخطيط لمقابلة الصحفيين الذين ينشرون معلومات غير دقيقة حول الديكريد. وكدليل اختباري  لسير هذا العمل، تم فحص إحدى المقالات السيئة من قبل المجتمع، و قد قام Ditto بجمع التعليقات الخاصة بهذه الحالة والحالات المستقبلية.Ditto  لديه [أنظمة](https://matrix.to/#/!OfChXgczrIlpEZSFAv:decred.org/$154690407510431bVTJQ:decred.org) لتسجيل كل قطعة من وسائل الإعلام المكتوبة عن الديكريد. وعندما يتعرفون على المجتمع بشكل أفضل ، سيكون من الممكن معالجة أوجه عدم الدقة في الوقت الحقيقي. كانت هناك مسألة أخرى تمت مناقشتها وهي [دمج سير الأعمال التصحيحية](https://github.com/xaur/decred-issues/issues/71) لDitto مع الطلبات الطوعية من المجتمع.
تم مناقشة شعار الديكريد على نطاق واسع في [marketing#](https://matrix.to/#/!OfChXgczrIlpEZSFAv:decred.org/$154711632712869dqRko:decred.org) و [Reddit](https://www.reddit.com/r/decred/comments/afctai/tagline_to_capture_the_decred_project/). النسخة النهائية من الرسائل استقرت على أن "الديكريد:  آمن، قابل للتكيف، ذاتي التمويل. " والتي تلقت الكثير من التأييد. مع مرور الوقت سيتم تنقيح كل هذا للتكيف مع التغيرات المستمرة للفضاء. 

### تحديث شهر يناير من Ditto:

* قمت بالبحث مرات عدة في وثيقة الرسائل الأساسية مع مساهمة كبيرة من المجتمع، وتلقيت تعليقات إيجابية على [النسخة النهائية](https://pastebin.com/E5L6u2RV). (مناقشات: الإصدار [الثاني](https://matrix.to/#/!OfChXgczrIlpEZSFAv:decred.org/$154706728112462ubmNo:decred.org)، الإصدار [النهائي](https://matrix.to/#/!OfChXgczrIlpEZSFAv:decred.org/$154880432321730DYSYl:decred.org)).
* عملت مع المجتمع لتحديد مصدر التعليقات على هجمات 51٪ لاستخدامها في المستقبل مع الصحفيين عند حدوث هجوم والذي من المحثم أن يحدث، الهدف هو الحصول على رسالة للديكريد أمام الصحفيين حتى عندما لا يكون هناك أي أخبار قوية لمشاركتها. 
* وقامت وسائل الإعلام بتدريب ثلاثة أعضاء للديكريد.
* التغطية الإعلامية المضمونة: [عرض مقال](https://www.forbes.com/sites/leslieankney/2019/01/11/who-should-hold-power-decred-governance-and-what-it-means-for-investors/#35955166e2ca) في الفوربس([تقرير](https://matrix.to/#/!OfChXgczrIlpEZSFAv:decred.org/$1547232200845NiZnO:decred.org))، [مقابلة فيديو](https://www.youtube.com/watch?v=CUxDxJ4YAUA) مع Joshua على Bitsonline، بيان بواسطة richardred@ حول التأخير في التفرع الصلب للإيثريوم في [Breaker Mag](https://breakermag.com/what-we-know-about-the-vulnerability-behind-ethereums-rollback-of-constantinople/) و [Crypto Briefing](https://cryptobriefing.com/scaling-delay-ethereum-constantinople/).
* صيغ إعلان برنامج مكافأة إيجاد العلل و تم [وضعه](https://hackernoon.com/decred-launches-debug-decred-bug-bounty-program-7e4d2af27ec9) في Hacker Noon -وبالتالي سيسهل ذلك الوصول إلى مجموعة أوسع بكثير من المطورين، مقارنة بقنوات الديكريد الخاصة. 
* ويسر إجراء مقابلتين انتظارا للتغطية الإعلامية.
* وتوجّه إلى مؤتمر بيتكوين في أمريكا الشمالية، حيث سهّل ديتو إجراء المقابلات بين الديكريد والمراسلين (Cheddar TV، Altcoin Buzz، إلخ) وقضى وقتًا ممتعًا مع الفريق.
* وقد عمل بشكل وثيق مع داستن حول وضع خطة للمناسبة والتي تشمل كلتا الفعاليات التي ترغب الديكريد في التحدث فيهما والفعاليات التي تود المشاركة فيها بكشك. 
* وقدم طلبًا لجيك للتحدث في توافق الآراء 2019.
* عمل بشكل وثيق مع داستن في خطة للتسويق والاتصالات في النصف الأول من عام 2019، تشمل الرسائل، التدريب الإعلامي، العلاقات الإعلامية، الفعاليات والتحدث، والاستراتيجية. هذه الخطة لا تزال معلقة.

وينصح الأفراد بتبادل التغطية الإعلامية لأن توسيع نطاق التغطية لا يقل أهمية عن وضع وسائط الإعلام نفسها.

لمزيد من التفاصيل، اطلع على تحديثات الأسبوعين في [7 يناير](https://matrix.to/#/!OfChXgczrIlpEZSFAv:decred.org/$154688457110052CiWYd:decred.org) و [18 يناير](https://matrix.to/#/!OfChXgczrIlpEZSFAv:decred.org/$15478384869864RTCsv:decred.org). اكتشاف جيد في واحد منهم:

> المجتمع يرحب بالأسئلة ويشجعها، حتى وإن كان الشخص الذي يطرح الأسئلة يخشى أن تكون أسئلته "غبية".” ولقد لاحظنا روح التعاون والاستعداد للمساعدة التي لم نراها في مجتمعات أخرى. إنه منعش!

### مسائل أخرى:

* و[يشاع ](https://matrix.to/#/!OfChXgczrIlpEZSFAv:decred.org/$15478503329998HCAzR:decred.org)أن Ditto يمكنه أن يرتب لحية مجنونة تخول للمرء أن يرتدي سترة فضية اللون للديكريد.
* قام anshawblack@[بوضع](https://matrix.to/#/!OfChXgczrIlpEZSFAv:decred.org/$154792069410439nSRtR:decred.org) بضائع الديكريد في جميع متاجر تسجيلات ميامي.
* تم [تجديد](https://www.reddit.com/r/decred/comments/ae07as/custom_decred_merch_with_19_discount_in_the/) متجر Decredible مع العناصر الإضافية وشعارات الديكريد الجديدة.
يمكن تخصيص جميع المنتجات وتعديلها.

إشعار عاجل: [تتوفر](https://www.reddit.com/r/decred/comments/ahalex/new_batch_of_stakey_plushies_available/) مجموعة جديدة من من اللعب المحشوة ل Stakey!

## الفعاليات 

الحضور:

* [مؤتمر البتكوين في أمريكا الشمالية](https://btcmiami.com/) في ميامي، الولايات المتحدة الأمريكية. الحضور كان منخفضا بشكل مفاجئ: فقد كان من المتوقع أن يصل عدد الأشخاص إلى 6 ألاف ولكن لم يسجل سوى حضور 1،8 ألف بعد الحدث. الحضور وعرض jy-p@ عن [تطبيقات ختم الوقت للبلوكشين](https://btcmiami.com/session/applications-of-blockchain-time-stamping/) وحتى عدد الحضور كان جيدا مقارنة بالعدد الإجمالي. وتم تدريب 3 أعضاء على وسائط الإعلام ووجدوا أنه مفيد، ومن المقرر تدريب سبع أعضاء آخرين.
 مستودع للقيمة: "آمن. قابل للتكيف. ذاتي التمويل " والرسائل المصاحبة، وسائل فعالة جدا للحديث عن الديكريد. وجد أنها الأكثر وضوحا وتأثيرا. التقرير الكامل مع وصلات إلى الصور والفيديوهات من [هنا](https://github.com/heyvj/decred-events/blob/master/reports/20190116-tnabc-miami.md). 
* [جولة OKEx العالمية](https://www.eventbrite.hk/e/okex-global-meetup-tour-2019-taiwan-tickets-54689867867) في تايبيه، تايوان. morphymore@ روى قصة الديكريد وكيف تعمل. "فمقارنة بسنة 2018 ، بدأ الناس يميزون الديكريد بشكل أفضل. بعض الناس أخبروني أنهم تعرفوا عن الديكريد من الترجمة الصينية التي قمت بها العام الماضي من أطروحة الاستثمار الخاصة بPlaceholder. كان ذلك مشجعاً للغاية ويظهر أن معرفة الناس عن الديكريد في تايوان في تزايد مستمر.([التقرير](https://matrix.to/#/!aNPTuiryMFmdMQWUzb:decred.org/$15478245399446fDEQa:decred.org) و[الصور](https://photos.google.com/share/AF1QipP07yyYIYSVQKIZTOvhui5arrVcINi8e84M3ENFp8pBm6g-gf8AXyTZ1e4rcwLwHg?key=MlRuX0RtR21TSV9qWUdDRE1yUTcwNHRWaTJBNENn)) 
* [10 lat Bitcoina](https://10latbitcoina.com.pl/) في وارسو ، بولندا. تحدث karamble@ عن  ديمومة العملات الرقمية مركزا على الديكريد. و أنشأ الفريق المكون من أربعة أشخاص علاقات مع عدد من منابر العملات الرقمية واشترك في عدد قليل من الأعمال التجارية. كما ذكر  BitHub.pl:"شارك فتيان الديكريد في الإجابة على الأسئلة من المهتمين مع إبداء الكثير من الصبر، حيث أن الأسئلة تدفقت في الأساس طوال الوقت!". ([التقرير](https://github.com/heyvj/decred-events/blob/master/reports/20190126-10LatBitcoina-Warsaw.md))

الأحداث القادمة:

* [حفلة الحرم الجامعي](http://brasil.campus-party.org/cpbr12/patrocinadores/) في ساو باولو، البرازيل في 12-17 فبراير.
* [كيف تؤمن عملاتك الرقمية](https://www.meetup.com/fr-FR/Decred-Australia/events/258211699/)، ملبورن، أستراليا في 18 فبراير. 
* [الديكريد في 30 دقيقة](https://www.eventbrite.com/e/decred-en-30-minutos-tickets-55764142050)، مكسيكو سيتي، المكسيك في 27 فبراير. لمزيد من المعلومات راسل elian@.
* [خاليسكو Talent Land](https://www.talent-land.mx/#entradas) في غوادالاخارا، المكسيك في 22-26 أبريل.اتصل بـ elian@ إذا كنت مهتمًا بالمساعدة / الحضور.

وقد نوقش وعرض في [هذا العدد](https://github.com/xaur/decred-issues/issues/83) فعاليات ذات إتجاه مفتوح المصدر مثل DEFCON وCCC وFOSDEM.

## وسائل الإعلام

مبادرات المجتمع:

* [blog.dcrclub.org](https://blog.dcrclub.org/) هو موقع إلكتروني جديد باللغة الصينية يجمع العديد من المقالات والترجمات في مكان واحد. المصدر المستضاف [على GitHub](https://github.com/0x5826/blog.dcrclub.org) يجعل من السهل المساهمة أو عكس موقع الويب على نطاق آخر لمزيد من المرونة. الإعتماد لTogT4V@ على Telegram  لبدء الموقع.
* [مدونة عربية جديدة](https://decred-arabia.blogspot.com/2019/01/blog-post.html) عن الديكريد بدأت بواسطة butterfly@ (أو arij@ على Matrix). هناك بعض التحديات مع نشر النص العربي على شبكة الإنترنت، ونرحب بالمشورة في  writers_room#.
*  michae2xl@[ بدأ](https://matrix.to/#/!kdpEDksmOMNrlMqffD:decred.org/$1548814257223928fVjiP:matrix.org) سلسة من الملفات الصوتية البرتغالية، وهي متوفرة على [Soundcloud](https://soundcloud.com/user-770106247/) وSpotify وApple Podcasts وGoogle Podcasts - ابحث عن "Decred Brasil".
* [decredexplorer@](https://twitter.com/decredexplorer) عبارة عن حساب Twitter جديد مخصص لـ dcrdata. شكرا لmichae2xl@ للتنظيم.
* و Matt D@ [قدم](https://matrix.to/#/!OfChXgczrIlpEZSFAv:decred.org/$154825336714293nfWdU:decred.org) على قناة التيليغرام [Decred Aggregator](https://t.me/DecredAgg). ويهدف إلى جمع الأخبار، الصحافة، مقاطع الفيديو، البودكاست، وإعلانات الديكريد، التغريدات الشائعة، ورسائل الريديت، بالإضافة إلى إحصاءات السوق.
* كما يخطط anshawblack@ لعمل بودكاست.

تم حذف [صفحة الديكريد](https://en.wikipedia.org/wiki/Decred) على ويكيبيديا. في 8 يناير قام مستخدم [بإزالة](https://archive.fo/ApV3P) مجموعة من "المصادر السيئة" وفي 10 يناير قام بتخريب الصفحة عن طريق إزالة جزء كبير ومهم من المحتوى. بعد 4 ساعات فقط رشح مستخدم آخر صفحة الديكريد للحذف - و كانت هذه [المحاولة الثالثة](https://en.wikipedia.org/wiki/Wikipedia:Articles_for_deletion/Decred_%283rd_nomination%29) لإزالتها. لمعلومات مرجعية، كان لمؤلف [الترشيح الثاني](https://en.wikipedia.org/wiki/Wikipedia:Articles_for_deletion/Decred_%282nd_nomination%29) للحذف [وجهات نظر](https://archive.fo/QAlRp) مثيرة للاهتمام حول النزاهة وتم [حظره](https://en.wikipedia.org/wiki/User:Prince_of_Thieves) باعتباره دمية جورب (شخصية مزوّرة). وفي 11 كانون الثاني / يناير، أعيد نقل المحتوى وتم حظر صاحب البلاغ على أنه " دمية جورب " ، ولكن في اليوم التالي، قام مستخدم آخر [بتطبيق الحذف](https://archive.fo/fZUHW) مرة أخرى دون ترك أي تعليق. بعد تقسيم الصفحة أصبحت صغيرة جدا وجميع المستعرضين [صوتوا](https://en.wikipedia.org/wiki/Wikipedia:Articles_for_deletion/Decred_%283rd_nomination%29) لحذفها بسبب عدم وجود مصادر حسنة السمعة. واعتبرت مراجع جميع المقالات الأخيرة المقترحة في وسائل إعلام التشفير الرئيسية [غير جيدة بما فيه الكفاية](https://archive.fo/4xwaN). وفي 18 يناير تم حذف الصفحة وإزالتها من [قائمة العملات](https://en.wikipedia.org/wiki/List_of_cryptocurrencies) التي تم تركها مع عملات أكثر وضوحا. وترد في [هذه المسألة](https://github.com/xaur/decred-issues/issues/79) تفاصيل وصلات بالمناقشات. محررو ويكيبيديا ذو ي الخبرة مرحب بهم للمساعدة.

مقالات مختارة (بالترتيب الزمني):
 
* فهم إدارة الديكريد بواسطة الدكتور بتكوين مترجم إلى الصينية،[qq.com](https://mp.weixin.qq.com/s/z3hzILiPBsLJR72Q2tP7TQ)، [الترجمة](https://translate.google.com/translate?sl=auto&tl=en&hl=en&u=https%3A%2F%2Fmp.weixin.qq.com%2Fs%2Fz3hzILiPBsLJR72Q2tP7TQ)، تم تفويته  في عدد دجنبر.
* التحليل الأساسي: الديكريد بواسطة Piotr Arendarski على [linkedin.com](https://www.linkedin.com/pulse/funadamental-analysis-decred-dcr-piotr-arendarski-ph-d/)
* كيف تتغلب على فصل شتاء العملات الرقمية؟ إبحث عن البساطة ودبر الطابع المعقد، بواسطة jy-p@ على  [coindesk.com](https://www.coindesk.com/how-to-last-the-crypto-winter-seek-simplicity-manage-complexity)، كما تم وضع الشعار بعد جمع الأفكار الجماعية على منتدى marketing#.
* الديكريد - مقابلة مع مدير المنتدى donmario@ بواسطة Janusz Zi على [bithub.pl](https://bithub.pl/wywiady/decred-wywiad-z-community-managerem/)
* أفضل محافظ الديكريد: أفضل 6 أماكن لتخزين DCR الخاص بك بواسطة ستيف والترز، [coinbureau.com](https://www.coinbureau.com/analysis/best-decred-wallets/)، من الجميل أن ترى المؤلفين متجاوبين وقاموا بتصحيح جميع [القضايا المبلغ عنها](https://github.com/xaur/decred-issues/issues/68)
* من يجب أن يتولى السلطة؟ إدارة الديكريد وما الذي تعنيه للمستثمرين بواسطة ليزلي انكني [forbes.com](https://www.forbes.com/sites/leslieankney/2019/01/11/who-should-hold-power-decred-governance-and-what-it-means-for-investors/)
* خارطة الطريق المستقلة للمقاولين لعام 2019، [medium](https://medium.com/decred/decred-independent-contractor-roadmap-884faba3db39)
* آلية توافق الآراء الفريدة من الديكريد -هل هذه اللامركزية الحقيقية؟ بواسطة بول دو هافيلاند [bitsonline](https://bitsonline.com/consensus-mechanism-of-decred-decentralization/)
* الديكريد كمستودع للقيمة بواسطة Yin Guochao، مستوحى من مقالة Forbes، مترجم إلى الصينية، [qq.com](https://mp.weixin.qq.com/s/_-lY0rtWSPiyLPZeTRR7gg)، [الترجمة](https://translate.google.com/translate?sl=auto&tl=en&hl=en&u=https%3A%2F%2Fmp.weixin.qq.com%2Fs%2F_-lY0rtWSPiyLPZeTRR7gg)
* مراجعة مشروع البلوكشين: الديكريد: 8.4 العملة الرقمية المستقلة بواسطة Evaluape على [medium](https://medium.com/@EVALUAPE1/blockchain-project-review-decred-8-4-autonomous-digital-currency-323771d65529) ،تم تقييم الديكريد 8.4/10.
* مراجعة عملة الديكريد: أتحل محل BTC؟ بواسطة ادوين، مترجم إلى الهولندية، [bitcoinsaltcoins.nl ](https://www.bitcoinsaltcoins.nl/decred-coin-review-vervanger-van-btc/) ، تم تقييم الديكريد 8.8/10
* 3 عملات رقمية تخزنها خلال فصل شتاء العملات الرقمية بواسطة Daniel Frumkin  على  [investinblockchain.com](https://www.investinblockchain.com/cryptocurrencies-hodl-during-crypto-winter/inblockchain.com)
* القيمة الأساسية في العملات الرقمية؛ البتكوين والديكريد كمخزن لاستثمارات القيمة بواسطة LCC Investment Research على [seekingalpha.com](https://seekingalpha.com/article/4235521-fundamental-value-crypto-bitcoin-decred-store-value-investments)
* دور الناخبين ذوي النفوذ في الدفاع ضد هجمات الأغلبية بقلم richardred@ على [medium](https://medium.com/@richardred/the-role-of-decred-voters-in-defending-against-majority-attacks-ec658af0a8fd).
* الحكم اللامركزي خارج السلسلة في سياق العملات الرقمية بواسطة Haon@   على [goodaudience.com](https://blog.goodaudience.com/decentralized-off-chain-governance-in-the-context-of-digital-currencies-ef6db7d97412)
* مقابلات الهيكل الأساسي للديكريد: ستيفن، مؤسس سوق السلع الفاخرة فقط، CryptoEmporium بقلم kozel@ على [medium](https://medium.com/@artikozel/decred-infrastructure-interviews-stephen-founder-of-crypto-only-luxury-goods-marketplace-68d3214a4fd7)
* مراجعة الديكريد بقلم Lee Banfield على [weeklyglobalresearch.wordpress.com](https://weeklyglobalresearch.wordpress.com/2019/01/31/decred-dcr-review/)

الترجمة:

* [تحليل مفصل لمقاومة تفرع الديكريد](https://medium.com/decred/detailed-analysis-of-decred-fork-resistance-93022e0bcde7) بقلم Haon@ -تمت ترجمته إلى [الروسية](https://medium.com/decred-russia/%D0%B4%D0%B5%D1%82%D0%B0%D0%BB%D1%8C%D0%BD%D1%8B%D0%B9-%D0%B0%D0%BD%D0%B0%D0%BB%D0%B8%D0%B7-%D1%83%D1%81%D1%82%D0%BE%D0%B9%D1%87%D0%B8%D0%B2%D0%BE%D1%81%D1%82%D0%B8-decred-%D0%BA-%D1%84%D0%BE%D1%80%D0%BA%D1%83-b30c78f764ea) بواسطة DZ@
* صحيفة الديكريد لشهر دجنبر 2018: تمت ترجمتها إلى: [الصينية](https://www.jianshu.com/p/65e7a83ac27c) بواسطة guang@، [البولندية](https://github.com/artikozel/DecredJournalPL/blob/master/journal/201812_DecredJournalPL.md) بواسطة kozel@، [البرتغالية](https://medium.com/@maiconjunge/jornal-decred-dezembro-de-2018-947c616b894f) بواسطة maiconjunge@، [الروسية](https://medium.com/decred-russia/decred-journal-%D0%B4%D0%B5%D0%BA%D0%B0%D0%B1%D1%80%D1%8C-2018-9528f7a9d24d) بواسطة DZ@، و[الإسبانية](https://medium.com/@decred_es/revista-decred-diciembre-2018-79093f957aac) بواسطة elian@. يا للروعة! شكرا لكم جميعا على نشر مذكرات الديكريد حول العالم! جميع الترجمات مدرجة [هنا](https://xaur.github.io/decred-news/).

أشرطة الفيديو:

* تطبيقات الختم الزمني للبلوكشين - بواسطة jy-p@ في TNABC ([اليوتيوب](https://www.youtube.com/watch?v=3RRTidXh_Lw))
* المقابلات التي أجريت في TNABC  [مع  joshuam@](https://www.youtube.com/watch?v=Kyihc6Uh4XA) بواسطة  Hack Crypto، [مع  joshuam@](https://bitsonline.com/decred-disputes-inevitable-buirski/) بواسطة Bitsonline ،  [مع DZ@](https://www.youtube.com/watch?v=h3bII-vjOsA)، [مع jz@](https://www.youtube.com/watch?v=4oKRVXGN6Fs) بواسطة CNBC Crypto Trader.
* الإدارة: عمود البلوكشين الأكثر تغييراً - بواسطة oregonisaac@ في منتدى العملات الرمزية 2  ([tfblock.io](https://www.tfblock.io/post/governance-blockchain-s-most-overlooked-pillar))

الصوتيات:

* لنأخذ نظرة عميقة حول العملات الرقمية المستقلة مع الديكريد - moo31337@ و BAB@ يتحدثان عن أن كيفية اتخاذ القرارات اللامركزية والتمويل الذاتي مكنا الديكريد من بناء عملة رقمية قوية ومتطورة خالية من نفوذ الطرف الثالث (بودكاست ل The Crypto Chick مع Rachel Wolfson على [badcryptopodcast.com](https://badcryptopodcast.com/2019/01/08/autonomous-crypto-decred/))
* إدارة البلوكشين مع  Noah Pierau: الديكريد، البتكوين، الداش، الإيثيريوم (51% من أبحاث العملات الرقمية بواسطة Tom Shaughnessy  على [itunes](https://itunes.apple.com/us/podcast/noah-pierau-on-blockchain-governance-decred-bitcoin/id1438148082?i=1000428113722&mt=2))
* كيف يغير الديكريد ثورة التمويل في العملات الرقمية مع ماركو بريبوم - مايكل ناي وماركو يناقشان الوضع الحالي للعملات الرقمية، كيف بدأ الديكريد، إثبات الحصة مقارنة بإثبات العمل، ونموذج تمويل الديكريد والمزيد (Evolvement Podcast على [evolvement.io](https://evolvement.io/how-decred-revolutionizes-funding-in-crypto-with-marco-peereboom/))

## مناقشات المجتمع

إحصائيات المجتمع اعتبارًا من 4 فبراير:

* متابعو التويتر:39,778 (106-)
* المشتركين في ريديت:9,330 (89+)
* مستخدمي الماتريكس:247 (26+)
* مستخدمي السلاك:6,529 (110+)
* مستخدمي التيليغرام:4,503 (231-)
*المشاركين في اليوتيوب:3,752 (14+)
* متابعي الفايسبوك:3,132 (11+)، إعجاب:2,891 (11+)
* متابعي LinkedIn: صفحة الديكريد 466 (16+)، صفحة بوليتيا 27 (3+)
* نجوم Github dcrd: زيادة عشرة نجوم 468(10+)، تفرع:1,221 (29+)

أخبار أنظمة الاتصالات:

* يستمر [نزيف تابعي](https://matrix.to/#/!OfChXgczrIlpEZSFAv:decred.org/$1549500437341uJIFK:decred.org) تويتر البطيء لأسباب غير معروفة. أي أفكار هي موضع ترحيب.
* هبوط في عدد مستخدمي التيليغرام من المحتمل بسبب تطهير الروبوت. 
* كتب sambiohazard@ [خطة](https://github.com/xaur/decred-issues/issues/16) شاملة لمعالجة مشكلة الرسائل المزعجة على Discord، قام بتنفيذها، ولم يبلغ عن أي رسائل مزورة بعد الأسابيع القليلة الأولى. كما تم وصل عدة قنوات مهمة مع Discord. مع هذا يمكننا أخيرا تقدير Discord كفرصة لجلب المزيد من الناس. شكرا لكم!
* يرشد [decred.org/matrix](https://decred.org/matrix/) مستخدمي الماتريكس الجدد إلى النظام.
* نمت [قضايا الديكريد](https://github.com/xaur/decred-issues) إلى 105 قضية اعتبارا من 9 فبراير. تحقق من ذلك، ربما ستجد شيئًا مثيرًا للاهتمام! 

وقد أثارت [إنتقادات](https://twitter.com/tonevays/status/1086702239853379584)  متطرفوا البتكوين [مناقشة](https://www.reddit.com/r/decred/comments/ahuawl/decred_launch_security_laws/) حول الكيفية التي ينظر بها الديكريد في سياق القوانين الأمنية. و كان رأي أحد النقاد أن التعدين القبلي للديكريد و توزيع airdrop  لم يكن عادلا و "تم اختيارهم يدويًا". هذا تمثيل خاطئ للجهد اليدوي (الضخم) لتصفية غشاشين airdrop، وفي [هذه المناقشة](https://matrix.to/#/!OfChXgczrIlpEZSFAv:decred.org/$154810656412322VrQLg:decred.org) العديد من الروابط المفيدة التي تصف كيفية إطلاق الديكريد. إحدى الأفكار المثيرة للاهتمام هي أن بعض القطع النقدية التي تم توزيعها و التي تبلغ ~300 آلاف (35%) لم تتحرك أبدًا. [دردشة](https://matrix.to/#/!kdpEDksmOMNrlMqffD:decred.org/$15467943549316LjeYZ:decred.org) أخرى ذات صلة، تهم هجمات التويتر والتي تدعي أن التوزيع الأولي للديكريد لم يكن شفافا أو نزيها ، مع تجنب الحقائق غير الملائمة حول التعدين المبكر للبتكوين والمليون BTC التي أخذها ساتوشي. وأخيرا، أوضح [درس في التاريخ](https://matrix.to/#/!MgQoetFiyjrHAywokv:decred.org/$15467944729319gvTvt:decred.org)  الأيام الأولى للتحصيص، وبين أن المطورين الأصليين لا يملكون أي سيطرة أحادية على قواعد الإجماع منذ اليوم الأول. 

نقاش ضخم حول أهمية بناء مجتمع على Reddit [هنا](https://www.reddit.com/r/decred/comments/aib2x3/noah_pierau_on_blockchain_governance_decred/).

## الأسواق

في كانون الثاني / يناير، كان يجري تداول  DCR ما بين 15.5 و 19.5 دولار أمريكي BTC 0.00435-0.00487 .  بلغ متوسط المعدل اليومي للتداول  17.1 دولار أمريكي.

## الخارجية ذات الصلة

تعرض الإيثريوم كلاسيك (ETC) لهجوم بنسبة 51 ٪ ، مع رفع التحذير بواسطة [CoinNess](https://www.coinness.com/news/198264) في 7  من يناير. ثم [أعلنت](https://blog.coinbase.com/ethereum-classic-etc-is-currently-being-51-attacked-33be13ce32de?gi=4f97315dfb30) شركة Coinbase أنها قد اكتشفت عملية إعادة تنظيم عميقة لسلسلة ETC وأوقفت معاملات ETC. تسرد المقالة عددًا من عمليات إعادة التنظيم التي تضمنت إنفاقًا مضاعفًا ، مما يضع إجمالي المبلغ في 1.1 مليون دولار ، عبر 15 حدثًا مختلفًا لإعادة التنظيم.لم تكن Coinbase نفسها هدفا لهذه الهجمات.بعد ذلك ، [أعلنت](https://blog.coinbase.com/ethereum-classic-etc-is-currently-being-51-attacked-33be13ce32de?gi=4f97315dfb30) منصة Gate.io للتبادل أنها استهدفت وفقدت حوالي 200 ألف دولار ، وأنها ستستوعب الخسارة. كما زاد Gate.io بشكل ملحوظ عدد التأكيدات المطلوبة لودائع ETC. في تطور غير عادي ، قام المهاجم [بإرجاع](https://www.gate.io/article/16740) 100 ألف دولار من ETC إلى Gate.io ، حاولوا ولكنهم فشلوا في الاتصال بالمهاجم ولا يعرفون سبب إرجاع الأموال.ولم يتقدم أي من الضحايا الآخرين للنفقات المزدوجة لETC.

[قرر](https://www.coindesk.com/ethereum-developers-give-tentative-greenlight-to-asic-blocking-code) مطورو شركة Ethereum (مؤقتًا) في 4 كانون الثاني (يناير) المضي قدماً في تغيير خوارزمية التعدين من Ethash إلى ProgPoW. تهدف هذه الخطوة إلى وقف ASICs من تعدين Ethereum.وقد [أوضحت](https://www.theblockcrypto.com/2019/01/11/despite-core-dev-consensus-proposition-progpow-faces-community-concerns/) The Block  المخاوف مثل انخفاض تكلفة الهجوم بعد التبديل، والحوافز الضعيفة للمعدنين في GPU ، والفوائد المشكوك فيها لنقل الطاقة من Bitmain و Innosilicon إلى AMD و Nvidia ، وانقسام محتمل للسلسلة. 
وخلصوا إلى أن النقاش حول تبديل الخوارزمية سيكون اختبارًا جيدًا لعملية إدارة Ethereum.

كما قام مطورو الإيثيريوم [بتأخير](https://breakermag.com/what-we-know-about-the-vulnerability-behind-ethereums-rollback-of-constantinople/) التفرع الصلب لConstantinople في 15 يناير بعد [اكتشاف ](https://medium.com/chainsecurity/constantinople-enables-new-reentrancy-attack-ace4088297d9)ضعف أمني كان من شأنه أن يمكن من "هجوم إعادة الدخول". 

أساسيات إثبات العمل من [مقالة](https://blog.sia.tech/fundamentals-of-proof-of-work-beaa68093d2b) David Vorick تقدم الحجج المؤيدة لأجهزة العملات الرقمية وتقارنها مع الأجهزة المشتركة للعملات الرقمية التي تعاني من مشكلات متعددة ، وخاصة أولئك الذين يسعون وراء مقاومة ASIC.وإحدى المسائل المتعلقة بالأجهزة غير المتخصصة هي أن قيمة المعدات لا ترتبط ارتباطا وثيقا بالموجودات (لأنها تستطيع إزالة العديد من السلاسل الأخرى).وهناك مسألة أخرى هي أسواق معدلات الهاش،  فهي تسمح لأصحاب الأجهزة بالحصول على ربح أكبر من خلال عدم الاهتمام بالعملة التي يتم تعدينها، حتى وإن كان معدل الهاش مؤجرا للمهاجمين. تستفيد الديكريد من الأجهزة المتخصصة، وهي إلى حد بعيد العملة المهيمنة لخوارزميتها (Blake256r14).على الرغم من أن هذه الأجهزة لا يمكن أن تعتبر "حصرية" للديكريد، بالإضافة إلى معدل الهاش المهيمن على الخوارزمية فالديكريد لديه عامل إثبات الحصة القادر على رفض المكافآت للمعدنين السيئين.

[انتهت](https://blog.aragon.org/final-results-from-aragon-network-vote-1/) الجولة الأولى من التصويت على اقتراح أراغون في 26 يناير.من بين المقترحات الـ 12 المقدمة ، تم استبعاد 3 من التصويت من قبل مؤسسة أراغون (1 بسبب الافتقار إلى القيادة الدائمة والمواهب الهندسية ، 2 استبعدت للحد من الحمل المعرفي على الناخبين). تمت [الموافقة](https://mainnet.aragon.org/#/governance.aragonproject.eth/0x277bfcf7c2e162cb1ac3e9ae228a3132a75f83d4) على 8 من المقترحات التسعة التي تم التصويت عليها من قبل حاملي ANT ، مع رفض اقتراح واحد (لتغيير مدة التصويت من 48 ساعة إلى أسبوع واحد). [تراوحت](https://mainnet.aragon.org/#/governance.aragonproject.eth/0x277bfcf7c2e162cb1ac3e9ae228a3132a75f83d4) معدلات المشاركة في ANT من 2.3 إلى 7.8٪.وسيدفع أغلى [اقتراح](https://github.com/aragon/flock/blob/master/teams/Aragon%20One/2019.md) سيوافق عليه أراغون مبلغ 4 ملايين دولار لتغطية تكاليف التشغيل لعام 2019 بالإضافة إلى مجموعة حوافز تتألف من 1.675 مليون ANT  على جدول التخويل لمدة 5 سنوات..تم تضمين حافز في ANT مع جدول استحقاق كجزء من معظم المقترحات ، بالإضافة إلى التكلفة الرئيسية التي يتعين دفعها في DAI.في المجموع ، ستكلف هذه الجولة من المقترحات المعتمدة حوالي 5.94 مليون دولار + 2.52 مليون ANT (حوالي 880 ألف دولار).

بدأ نظام استفتاء EOS للتعديلات الدستورية [مباشرة](https://medium.com/@eosnationbp/the-fate-of-eos-is-in-the-hands-of-token-holders-3d345147ef6) في 11 يناير. وقد تم حتى الآن [تقديم](https://bloks.io/vote/referendums) 77 اقتراحا. فترة التصويت على هذه المقترحات مرنة ومحددة من قبل مقدم الطلب ، وبعضها يستمر لمدة تصل إلى أربعة أشهر. حصلت المقترحات التي حازت على أكبر عدد من الأصوات (اعتبارًا من 31 يناير) على أصوات من حوالي 2٪ من EOS المتداولة ، ولكن معظم المقترحات لها مشاركة منخفضة جدًا (10 مشاركات فقط تزيد عن 0.5٪).وحتى الآن ، فإن أكثر المقترحات شعبية هي [تغيير](https://bloks.io/vote/referendums/rex4all) المكان الذي تذهب إليه رسوم الأسماء القصيرة وعمليات شراء ذاكرة الوصول العشوائي ، و[حذف](https://bloks.io/vote/referendums/decaf) منتدى EOS Core Arbitration Forum ، و[حرق](https://bloks.io/vote/referendums/burnsaving) صناديق التضخم في eosio.saving (لاستخدامها في تمويل نظام اقتراح العمال).

[أعلنت](https://forum.nem.io/t/nem-foundation-message-to-the-community/21753) مؤسسة NEM بأنها تواجه صعوبات مالية وتحتاج إلى تقليص حجم قوتها العاملة.مجلس جديد تولى المؤسسة في 1 يناير وعندما فتحوا الكتب وجدوا مشكلة. وكان معدل الحرق في المجلس السابق 9 ملايين xem شهريا (360k الآن ، أي أكثر بكثير في ذلك الوقت) أنفقته كيانات إقليمية مستقلة على الأنشطة الترويجية دون مساءلة تذكر.واعتبر ذلك غير قابل للاستمرار، وقد أعاد المجلس الجديد هيكلة المؤسسة ويسعى حاليا إلى الحصول على أموال إضافية.

تم [نشر](https://hackernoon.com/towards-an-analytical-discipline-of-forkonomy-summer-2018-e6da993ee3f9) نسخة محدثة من بحث "forkonomy" من قبل وسيم السندي (parallelind@) مع [متابعة حديثة](https://hackernoon.com/forkonomy-revisited-where-are-they-now-73fbfbec6b4d).

قام Hcash بتفريع [بضعة](https://archive.fo/rEhWX) مشاريع أخرى للديكريد: : Autonomy (Politeia)، hcexplorer و hctime. في بوليتيا، [أزالوا](https://archive.fo/ECplt) عرضيا حقوق التأليف والنشر لمطوري الديكريد ونسوا إعادة تسمية المشروع. وبعد إبلاغهم ، استجابوا بسرعة بإزالة المستودعات المتعددة ، و[إعادة](https://github.com/TKFORKED/autonomy/commit/4b05c2c31829df64be69e546d939a563247e1927) الترخيص مع [إعادة تسمية](https://github.com/TKFORKED/autonomy/commit/98d5f63f676e45e6a91eba99da3db985effdb1f2) Politeia fork ب  Autonomy. كما  تم إصلاح بعض الأيقونات المهترئة و [الخفية](https://twitter.com/michae2xl/status/1084270468234915840) للديكريد. وقد تم تفريع بعض [المشاريع](https://archive.fo/https://github.com/HcashOrg/hc*) مع مسح تاريخ التزامهم دون وضع علامات عليها كتفرعات على GitHub. تم [حجب](https://archive.fo/Edy7T) الشكاوى ([1](https://www.reddit.com/r/hcash/comments/adwmx2/hcash_being_shady_again/) ، [2](https://www.reddit.com/r/hcash/comments/afepsc/hcash_cant_be_bothered_to_change_the_decred_logo/)) على subreddit بصمت مع عدم الرد. أوه ، وأساليب [r / hcash](https://archive.fo/Edy7T) تبدو [مألوفة](https://archive.fo/e1rAw). نوقشت [هنا](https://matrix.to/#/!MgQoetFiyjrHAywokv:decred.org/$154696507010921TRgid:decred.org).

[مثال محزن](https://twitter.com/BrianDColwell/status/1090286752831434752) لما يمكن أن يحدث عندما ينفد الفريق من المال.

[سحبت مشاريع](https://diar.co/ethereum-ico-treasury-balances/) ICO ما يقارب ~441 آلاف ETH (52.5 مليون دولار اعتبارا من 9 فبراير) من سندات الخزانة في ديسمبر 2018. 

قامت [Staked](https://staked.us/about/) ، وهي شركة ناشئة تقدم خدمات مساندة للمستثمرين المؤسسيين ، بجمع 4.5 مليون دولار من Pantera و Coinbase و DCG وغيرها.والتي تغطيها [CoinDesk](https://www.coindesk.com/pantera-coinbase-join-4-5-million-round-in-staking-as-a-service-startup) ، و[The Block](https://www.theblockcrypto.com/2019/01/31/winklevoss-twins-pantera-get-behind-a-new-business-thats-capitalizing-on-a-new-trend-sweeping-crypto-hedge-funds/) و [Bloomberg](https://www.bloomberg.com/news/articles/2019-02-01/some-crypto-investors-are-playing-it-safe-after-volatile-run). تشغّل شركة Staked مزودًا [موفرًا لنظام التصويت](https://decred.staked.us/) للديكريد منذ نوفمبر 2018.

[يسمح](https://support.binance.com/hc/en-us/articles/360022498052) Binance الآن بشراء العملات الرقمية بواسطة Visa و MasterCard (و[قائمة القيود](https://support.binance.com/hc/en-us/articles/360022204152) تخبرنا بشيء عن fiat).

[حظرت](https://cryptocoinspy.com/coinbase-bans-gab-again/) Coinbase حسابات وسائل الإعلام لمنصة Gab.هذه ليست [الحالة الكبيرة الأولى](https://www.cnbc.com/2018/04/23/coinbase-suspends-wikileaks-bitcoin-account.html) لتعليق الحساب من منصة التبادل.

وقامت Medium [بفرض الرقابة](https://bitcoinist.com/how-to-use-bitcoin-anonymously-ban-medium/) على مقال  "كيفية استخدام البتكوين بشكل مجهول" ، الأمر الذي حفز النقاش و[مسألة](https://github.com/xaur/decred-issues/issues/70) الإنتقال منها، أو على الأقل التعامل معها على أنها واحدة من المحتويات ذات المرايا.إحتفظوا بنسخ إحتياطية لمنشوراتكم على Medium، تحسبا.

وأصدر مصرف التسويات الدولية [دراسة](https://www.bis.org/publ/work765.htm) متفائلة جدا عن العملات الرقمية.

تم اكتشاف [الضعف](https://cryptoslate.com/researchers-discover-vulnerability-bitcoin-ethereum-ripple-digital-signatures/) في التوقيعات الرقمية للبتكوين وبعض الأنظمة الأخرى.تم إنشاء مجموعة صغيرة من التوقيعات باستخدام تنفيذ خاطئ لخوارزمية التوقيع التي يمكن استخدامها للكشف عن المفاتيح الخاصة.فقط بضعة آلاف توقيع كانت ضعيفة من بين ما يقرب من مليار توقيع بتكوين تم فحصها.ووفقا للباحثين، فإن الغالبية العظمى من مستخدمي العملات الرقمية لا يحتاجون للقلق.

أكبر [خرق للبيانات](https://www.troyhunt.com/the-773-million-record-collection-1-data-reach/) في التاريخ يحتوي على مجموعة من الآلاف من قواعد البيانات التي تم الاستيلاء عليها.اختر بحكمة مع من تشارك البيانات.

تم [اختراق](https://www.investinblockchain.com/cryptopia-hack-estimated-16-million-lost/) cryptopia مع تقديرات للخسائر تتراوح بين 3-16 مليون دولار.وقد قام Binance بتجميد بعض الأموال القادمة من الإختراق.

تم [الإبلاغ](https://www.zdnet.com/article/new-ransomware-strain-is-locking-up-bitcoin-mining-rigs-in-china/) عن موجة جديدة من عدوى HAnt (تمت مشاهدتها لأول مرة في أغسطس) تستهدف أجهزة التنقيب عن البتكوين.الفيروس يطالب بإصابة 1000 أجهزة أخرى أو دفع 10 BTC ، وإلا فإنه يهدد بحرق الجهاز.لم ترد أي تقارير عن تدمير المعدات حتى الآن.

تم [اكتشاف](https://medium.com/@dsl_uiuc/fake-stake-attacks-on-chain-based-proof-of-stake-cryptocurrencies-b8b05723f806) الضعف الناتج عن استنفاد الموارد المعروف باسم Fake Stake attack في أزيد من 26 سلسلة كتلة بناءا على PoSv3، معظمها  خففت من حدة الإنتشار. جزء من السبب هو أن في كثير من هذه الأنظمة كانت طبقة إثبات حصة "مطعمة" بقاعدة بيانات Bitcoin Core بشكل غير آمن. واحد من مؤلفي التقرير غرد بأن الديكريد [لم يتأثر](https://twitter.com/Sanket1729/status/1087829688347701254). 

## حول هذا العدد

هذا هو العدد العاشر من مجلة الديكريد.ويوجد [هنا](https://xaur.github.io/decred-news/) فهرس لجميع الأعداد السابقة والمرايا والترجمات. 

ويتم نقل معظم المعلومات الواردة من أطراف ثالثة مباشرة من المصدر بعد التحقق من صحتها. لا يملك مؤلفو صحيفة الديكريد أي قدرة على التحقق من جميع الادعاءات. رجاء إحذر من أعمال الاحتيال وقم ببحثك الخاص.

نرحب بتعليقاتك ومساهماتك على Reddit و [GitHub](https://github.com/xaur/decred-news/issues) و [Matrix](https://matrix.to/#/!lbzTjhzNbIaDbuAxkS:decred.org).

الاعتمادات (بالترتيب الأبجدي): 
- bee
- davecgh
- degeri
- Dustorf
- guang
- Haon
- jholdstock
- liz_bagot
- lukebp
- matheusd
- richardred
- saender
- zubairzia0.

قم بزيارة مجلة الديكريد الكاملة باللغة الإنجليزية على الرابط التالي: [رابط الصفحة](https://xaur.github.io/decred-news/journal/201901.html).

الترجمة إلى العربية: butterfly@

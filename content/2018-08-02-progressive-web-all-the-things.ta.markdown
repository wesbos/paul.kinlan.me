---
slug: pwa-progressive-web-all-the-things
date: 2018-08-02T14:56:13.506Z
title: 'PWA: Progressive Web All-the-things'
description: ""
tags: ['pwa']
---


PWA. முற்போக்கான வலை பயன்பாடுகள். பிரான்சஸ் பெர்ரிமான் மற்றும் அலெக்ஸ் ரஸ்ஸல் ஆகியோர் 2015 ஆம் ஆண்டில் "முற்போக்கான வலைப் பயன்பாடுகள்" என்ற வார்த்தையை உருவாக்கியுள்ளனர். "முற்போக்கான வலைப் பயன்பாடுகள்: எமது சோலை இழக்காமல் தாவல்கள் தப்பித்தல்" (0) ".

3 ஆண்டுகள் கழித்து, நாங்கள் நீண்ட தூரம் வந்துள்ளோம். தொழிலாளர்கள் மற்றும் டெவலப்பர்களால் தொழில்துறையுடன் ஒட்டிக்கொள்ள ஆரம்பித்த ஒரு பிராண்டுக்கு, ஒரே ஒரு உலாவி என்ஜினில் மட்டுமே நடைமுறைப்படுத்தப்பட்டது, மற்றும் அனைத்து முக்கிய நிறுவனங்களுடனும் - சேவை தொழிலாளி, மேனிஃபெஸ்ட், ஹோஸ்ஸ்கிரீன், வெப் புஷை சேர் 'பி.டபிள்யு.ஏ' ஸ்டாக் பெரும்பான்மையை உலாவி விற்பனையாளர்கள் அமல்படுத்துகின்றனர்.

காட்டுப்பகுதியில் எத்தனை PWA கள் உள்ளன என்பதைப் புரிந்துகொள்ள எங்களுக்கு உதவுகின்ற [app](https://appsco.pe/) [directories](https://pwa-directory.appspot.com/), [கருவிகள்](https://blog.tomayac.com/2018/07/09/progressive-web-apps-in-the-http-archive-143748) இப்போது கிடைத்துள்ளன. PWA] (3). ஆனால் என்ன ஒரு PWA வரையறுக்கிறது? ஃபிரான்சும் அலெக்ஸ் இந்த பட்டியல்களின் பட்டியலைக் கொண்டு வந்தார்:

> **[Responsive](http://alistapart.com/article/responsive-web-design)**[:](http://alistapart.com/article/responsive-web-design) 
> to fit any form factor  
> **Connectivity independent**: Progressively-enhanced with [Service 
> Workers](http://www.html5rocks.com/en/tutorials/service-worker/introduction/) 
> to let them work offline  
> **App-like-interactions**: Adopt a Shell + Content application model to create 
> appy navigations & interactions  
> **Fresh**: Transparently always up-to-date thanks to the Service Worker update 
> process  
> **Safe**: Served via TLS (a Service Worker requirement) to prevent snooping  
> **Discoverable**: Are identifiable as "applications" thanks to 
> [W3C](https://w3c.github.io/manifest/) 
> [Manifests](https://developers.google.com/web/updates/2014/11/Support-for-installable-web-apps-with-webapp-manifest-in-chrome-38-for-Android) 
> and Service Worker registration scope allowing search engines to find them  
> **Re-engageable**: Can access the re-engagement UIs of the OS; e.g. [Push 
> Notifications](https://developers.google.com/web/updates/2015/03/push-notificatons-on-the-open-web)  
> **[Installable](https://developers.google.com/web/updates/2015/03/increasing-engagement-with-app-install-banners-in-chrome-for-android?hl=en)**[: 
> to the home screen through browser-provided 
> prompts](https://developers.google.com/web/updates/2015/03/increasing-engagement-with-app-install-banners-in-chrome-for-android?hl=en), 
> allowing users to "keep" apps they find most useful without the hassle of an 
> app store  
> **Linkable**: meaning they're zero-friction, zero-install, and easy to share.
> The social [power of
> URLs](http://www.theatlantic.com/technology/archive/2012/10/dark-social-we-have-the-whole-history-of-the-web-wrong/263523/)
> _matters_.


முக்கியமாக, நாம் எப்படி இணையத்தை பார்க்க விரும்பினோம் என்பதையும், எங்களுடைய தளம் ஒரு 'PWA' இல்லையா என புரிந்து கொள்ள உதவியது (கருவிகள்) கிடைத்ததைப் பற்றியும் கொஞ்சம் கொஞ்சமாக எங்கிருந்தாலும் இந்த விளக்கம் குறிக்கப்பட்டது. அலெக்ஸ் மேலும் மேலும் சென்று [PWA 'PWA](https://developers.google.com/web/tools/lighthouse/) தயாரிக்கும் தொழில்நுட்ப அம்சங்கள் சிலவற்றை வரையறுத்துள்ளார்.

இந்த இடுகையின் மிகுதியால் வழிவகுக்கும் போது, ​​எல்லோரும் இந்த விஷயங்களைக் கட்டுவது ஏன்? [சரி, அது கடினமாக இருக்கலாம். மிகவும் கடினமாக உள்ளது (0). டெவலப்பர்கள் மற்றும் வணிகங்களை நாங்கள் நிறைய செய்யும்படி கேட்கிறோம். சில நேரங்களில் AppShell இல் கவனம் செலுத்துவது தளத்தின் முழுமையான மறு-கட்டமைப்பு ஆகும், மற்ற சமயங்களில் [AppShell 'சரியான கட்டமைப்பு அல்ல](/challenges-for-web-developers/). பல சந்தர்ப்பங்களில் மதிப்பு அல்லது கதை எப்போதும் தெளிவாக இல்லை.

நான் இணையத்தில் தங்கள் கவலைகள் கட்டிடம் பற்றி வணிகங்கள் மற்றும் டெவலப்பர்கள் நேரடியாக பேச முடியும் போதுமான அதிர்ஷ்டம், குறிப்பாக நான் வணிகங்கள் மற்றும் டெவலப்பர்கள் PWA பற்றி சொல்கிறேன் என்று விஷயங்கள் உள்ளன:

> We've got our site... but we are also making a PWA.


> &mdash; Many B2B sites we spoke (actually, I saw this a lot in India)


சுவாரஸ்யமான. அவர்கள் வித்தியாசமாக இருக்கிறார்களா? அடிக்கடி இல்லை, ஆனால் PWA ஒரு 'விஷயம்' அவர்கள் பற்றி கேள்விப்பட்டேன் மற்றும் அது தொடங்க மற்றொரு தயாரிப்பு தான். M போன்ற தளங்கள் டெஸ்க்டாப் தளத்தின் மொபைல் பதிப்புகளாக இருந்தன, PWA இன் இன்னொரு விஷயத்தை அவர்கள் தொடங்க வேண்டும்.

> I've got a PWA. It just does Push notifications.


> &mdash; Too many people.


வா. அது ஒரு PWA இல்லை, அது சொந்த பயன்பாடுகள் என்று தொழில்நுட்ப ஒரு துண்டு பயன்படுத்தி தான்.

> I'm only building a blog... it's not a PWA


> &mdash; Many bloggers we spoke to.


ம்ம். இது உள்ளடக்கத்தை தளங்களுக்கு நகர்த்துவதற்கான முக்கியம் என்பதற்கு ஏன் தெளிவுபடுத்த முடியவில்லை என்பது தெளிவாக உள்ளது.

> I don't care about making it installable.. I don't need a Service Worker.


> &mdash; Many publishers we spoke to.


ஹே. ஆப்ஸ் நிறுவல்களை நிறுவுகிறது, மற்றும் ஒரு தளம் அல்லது அனுபவம் பயன்பாட்டை நிறுவ வேண்டும் என நினைக்கும் கருத்து சிலவற்றில் இருந்து முற்றிலும் மாறுபடும். 2015 இல் ஒரு சுவாரஸ்யமான விவாதம் இருந்தது [கேரட்](https://trib.tv/2015/10/11/progressive-apps/) நான் உங்களை நீக்குமாறு ஊக்குவிக்கிறேன்.

> I don't need an app on desktop. I just need users to click 'checkout'


> &mdash; Many retailers we spoke to.


சரி. அது மிகவும் தெளிவாக இருக்கிறது. ஒரு பயனருக்கு அல்லது வணிகத்திற்கான மதிப்பானது அங்கு இல்லை, மேலும் PWA இன் பண்புகளை முன்னுரிமை செய்யும் ஒரு வணிகத்தை நிறுத்துவது போதுமானது.

> Progressive Web Apps are just better sites.


> &mdash; Many developers we speak to.


உண்மையில் நான் பெரிய வலை டெவலப்பர்கள் நிறைய இந்த நிறைய கேட்க.

நீண்ட காலமாக PWA இல் 'பி.டபிள்யு.ஏ' ஐ தள்ளி வருகின்ற ஒரு சமீபத்திய பேச்சு ஒன்றில், [ஜெர்மி கீத்](https://adactio.com/) எழுதியவற்றை சரிபார்க்க நான் உங்களை ஊக்கப்படுத்துகிறேன்.

> There's a common misconception that making a Progressive Web App means
> creating a Single Page App with an app-shell architecture. But the truth is
> that literally any website can benefit from the performance boost that results
> from the combination of HTTPS + Service Worker + Web App Manifest.


> &mdash; Jeremy Keith. "[Any Site can be a Progressive Web 
> App](https://noti.st/adactio/d1zSa7/any-site-can-be-a-progressive-web-app)" 


என் தனிப்பட்ட உணர்வு எல்லோரும் உண்மையில் PWA ஒரு ஏ மீது தொங்கிக்கொண்டு உள்ளது: 'ஆப்'. இது கருத்து முத்திரைக்கு வெற்றி மற்றும் தோல்வி தான்; 'பயன்பாடு' பெயரில் உள்ளது, 'ஆப்' என்பது பல பயனர்கள் மற்றும் வியாபாரங்களின் நனவில் உள்ளது, எனவே சங்கங்கள் மிகவும் தெளிவானவை.

முற்றிலும் தெளிவாக இருக்க வேண்டும், நானும் எங்கள் அணியில் உள்ள பலரும் PWA இன் சூழலில் 'ஆப்' சொற்களில் கடினமாக தள்ளி, குறிப்பாக மொபைல் சொந்த அனுபவங்களைப் போட்டியிடும் வகையில். [ஆண்ட்ரூ பெட்ஸின் இடுகை](https://trib.tv/2016/06/05/progressively-less-progressive/) எங்கள் அசல் நிலைப்பாட்டிற்கு எதிராக ஒரு நல்ல சுருக்கத்தை கொண்டிருந்தது, அதே சமயத்தில் நாங்கள் தவறாக நினைக்கவில்லை எனில், மொபைல் மையம் இல்லாதபடி, .

நாங்கள் Chrome Web Store ஐப் பற்றி பேசுகையில் இதைப் பார்வையாளர்களிடம் கேட்டேன். Gmail ஒரு பயன்பாடு அல்லது தளம்? ஒரு பயன்பாடு, அது எளிது. ட்விட்டர் ஒரு பயன்பாடு அல்லது தளம்? ஒரு பயன்பாடு .. இல்லையா? நான் உள்ளடக்கத்தை படித்துக்கொண்டிருந்தால், அது ஒரு இணைய தளம் போல உணர்கிறது. விக்கிப்பீடியா ஒரு பயன்பாடு அல்லது தளம்? ஒரு தளம், முற்றிலும்; அது போதும்? ஒரு ஆசிரியராக ஒரு கருவியைப் போல அது உணர்கிறது.

இறுதியில், ஒரு தளம் ஒரு பயன்பாடாகவோ அல்லது ஒரு பயன்பாடாகவோ இருந்தால் அது உண்மையில் மிகவும் முக்கியமானது என்று நான் நினைக்கவில்லை. இணையம், பொழுதுபோக்கு, பப்ளிஷிங், யூனிட்ஸ், காமர்ஸ் - இணையம், 'பயன்பாடுகள்', விளையாட்டுகள், வி.ஆர். பாபின்ஸ், சில்லறை விற்பனை கடைகள் அல்லது பாரம்பரிய 'தளங்கள்' போன்ற அனைத்தையும் உருவாக்கலாம்.

PWA இன் அசல் வரையறையை நீங்கள் கிண்டல் செய்தால், 'installability' ('பைக் கேரட்' பார்க்கவும்) தவிர, யாரும் வாதிடலாம் என்று ஒரு டெவலப்பர் தங்கள் தளத்தை மேம்படுத்தும் புள்ளிகள் ஏதேனும் ஒன்றை அலெக்ஸ் குறிப்பிட்ட பிறகு பயனர்கள் சிறந்த அனுபவத்தைப் பெறலாம், மேலும் பயனரின் சிறந்த அனுபவத்தைப் பெறுகையில், இணையத்தை மதிக்கிறார்கள் மேலும் மேலும் மக்கள் இணையத்துடன் ஒரு அர்த்தமுள்ள நிச்சயதார்த்தத்தை வைத்திருக்கிறார்கள் மற்றும் இணையத்தைப் பயன்படுத்துகின்றனர். எனவே ஒவ்வொரு வர்த்தகமும் டெவெலப்பரும் என்ன கவனம் செலுத்த வேண்டும் என்பதைப் பற்றி PWA கதைகளை எப்படிப் பயன்படுத்துவது?

---

நான் தொழில் துறையில் பார்த்துள்ள சவால்களை அடிப்படையாகக் கொண்ட சிறிய பிணைப்பைப் பற்றி யோசித்து வருகிறேன், டெவலப்பர்கள் மற்றும் தொழில்கள் தங்கள் முயற்சிகளை மையமாகக் கொண்டிருக்கும் முக்கியத்துவத்தை முன்னுரிமைப்படுத்த நான் முயன்றேன். (குறிப்பு: நான் [BizKin](https://twitter.com/business_kinlan) ஐ சேமிக்கும்

வணிகங்கள் மற்றும் டெவெலப்பர்கள் வெற்றிபெறுவதன் மூலம் இணையத்தின் தனித்துவமான திறன்களை வழங்குவதன் மூலம் வெற்றிபெற வேண்டும்: ஒரு பொத்தானைக் கிளிக் செய்வதன் வாயிலாக மிக அதிகமான பயனர்களை அடையலாம்; ஒற்றை தொகுப்பு குறியீட்டுடன் சாதனங்கள் முழுவதும் சிறந்த அனுபவங்களைக் கொண்டு அவர்களின் பயனர்களை தக்கவைத்துக்கொள்ளுங்கள்; மற்றும் அவர்களோடு நேரடியான மற்றும் சொந்தமான உறவைக் கட்டியதன் மூலம் அவர்களின் பயனர்களுடன் அர்த்தமுள்ள வகையில் ஈடுபட வேண்டும்.

நான் இணையத்தை பயன்படுத்தும் போது பயனர் உணர வேண்டும் என்று ஒரு கொள்கைகள் தொகுப்பு இந்த வெளிப்படுத்த முயற்சி. உங்கள் அனுபவம் இருக்க வேண்டும்: கண்டுபிடித்து, பாதுகாப்பானது, விரைவானது, மென்மையானது, நம்பத்தக்கது, முக்கியமானது

அதைத் தெரிந்து கொள்ளுங்கள்: உங்கள் அனுபவத்தை கண்டறிய பயனர்களை இயக்குங்கள். வலை இணைப்புகள் மற்றும் பக்கங்களினால் செய்யப்பட்டதாகும். எந்தவொரு தளத்திலிருந்தும் எவரையும் அனுப்ப முடியும் என்பதால், ஒவ்வொரு பக்கமும், மாநிலத்திற்கும் ஆழமான இணைப்பு இருக்க வேண்டும், அது ஒரு ஒருங்கிணைப்பாளர், செய்தி, ஒரு மின்னஞ்சல் அல்லது விளம்பர பலகை. எந்த ரெண்டரரும் அதை படிக்க முடியும் என்பதற்காக உள்ளடக்கம் வழங்கப்பட வேண்டும்.

பாதுகாப்பாக இருங்கள்: இணையத்திலும், உள்ளடக்க உரிமையாளர்களாலும் இணையத்தில் கட்டப்பட்ட அனுபவங்களை நம்பலாம், அடையாளம், இரகசியத்தன்மை மற்றும் தரவு ஒருமைப்பாடு ஆகியவற்றைப் பாதுகாக்கும்.

அதை வேகமாக செய்ய: பயனர் உங்கள் தளத்திற்கு இணைந்தவுடன், அவர்கள் உடனடியாக தட்டினால், அவர்கள் உங்கள் அனுபவத்தில் உள்ளனர் மற்றும் பயனர் கொண்டுள்ள நெட்வொர்க் அல்லது சாதனத்தைப் பொருட்படுத்தாமல் அதைப் பயன்படுத்தத் தொடங்கலாம்.

அதை மென்மையான செய்ய: பயனர் உங்கள் தளத்தில் இருக்கும் போது அனுபவம் அனைத்து பயனர் சைகைகள் பதிலளிக்க மற்றும் ஊடாடும். அனிமேஷன்கள் மென்மையான மற்றும் மிருதுவான உணர்வை உணர்கின்றன, பின்னூட்டம் உடனடியாக இருக்கிறது, ஸ்க்ரோலிங் மென்மையானது, வழிகாட்டிகள் உடனடியாக உள்ளன. [RAIL](https://developers.google.com/web/fundamentals/performance/rail) அடிப்படையில் வலை செயல்திறனை நீங்கள் கருத்தில் கொண்டால், நீங்கள் 'RAI' இல் கவனம் செலுத்துகிறீர்கள்.

அதை நம்பகமானதாக்கவும்: நம்பமுடியாத நெட்வொர்க் அல்லது சாதனங்களை எதிர்கொள்ளும் போது உங்கள் தளத்தின் பயனர்கள் முடிந்தவரை சில குறுக்கீடுகளைக் காணலாம். பயனர் எங்கிருந்தாலும் அனுபவம் வேலை செய்ய வேண்டும் மற்றும் பதிலளிக்க வேண்டும்.

இது அர்த்தமுள்ளதாக இருங்கள்: நீங்கள் மதிப்பை வழங்க வேண்டும் மற்றும் மதிப்பை வழங்கும் உயர் தரமான அனுபவங்கள் மூலம் உங்கள் பயனர் தேவைகளை பூர்த்தி செய்ய வேண்டும். இது மிகவும் பளபளப்பானதாக தோன்றலாம், ஆனால் [டியான் அல்மார் அதை நன்றாக விவரிக்கிறார்](https://medium.com/ben-and-dion/mission-improve-the-web-ecosystem-for-developers-3a8b55f46411). கவனம் உங்கள் தளத்தில் பயனர் தேவை ஒரு தீர்வு தீர்க்கும், இது பொழுதுபோக்கு, ஒரு கொள்முதல், அறிவு முன்னேற்றம் அல்லது ஒரு பணியை விரைவாக முடிக்க எளிதாக்குவது பற்றி உண்மையில் உள்ளது. இது UX பற்றி தான்.

** வேகமாக, நம்பகமான, பாதுகாப்பான மற்றும் மிருதுவான ** இந்த கொள்கை இலக்குகளை சந்திக்கும் ஒரு நவீன அனுபவம். இது திறந்த வலை மற்றும் அதன் மையத்தின் முற்றுப்பெறல் மூலம் நவீன API கள் மற்றும் மிகவும் ** கண்டறியக்கூடிய ** ஐப் பயன்படுத்தி படிப்படியாக அதிகமான செயல்திறன் **. ஒரு PWA இயற்கையாகவே பயனர் எதிர்பார்ப்புகளை அடிப்படையாக இந்த ஒவ்வொரு "கொள்கை இலக்குகளை" சந்தித்து மேலும் தொழில்நுட்பங்கள் மற்றும் திறன்களை உள்ளே அனுபவம் தொடர்ந்து உருவாக்க வேண்டும் ஆனால் இன்று இணையத்தில் எந்த நவீன அனுபவம் வேண்டும் ....

<span><span id='pw'>முற்போக்கு வலை</span> <span id=name>பயன்பாடுகள்</span></span> - முற்போக்கு வலை அனைத்து விஷயங்கள்.

அடுத்த வருடத்தில் நான் PWA ஐத் தள்ள விரும்புகிறேன். நீங்கள் என்ன நினைக்கறீர்கள்?

_ நன்றி ஹாரிலே பாத்ராவுக்கு.

{{ <html> }}

<style> dt {   font-weight: 600;   margin-bottom: 0.8em; } dd {   margin-bottom: 1em; } #pw {   font-weight: 700;   font-size: 1em; } #name {   font-size: 1em;   font-weight: 100; } </style><script>   const nameEl = document.getElementById('name');   const names = ['Apps', 'Sites', 'Stores', 'Blogs', 'Forums', 'Magazines', 'Block-chain doo-dads', 'Experiences', 'Wikis', 'Utilities', 'Games'];   let counter = 1;   setInterval(()=> {      nameEl.textContent = names[counter];     counter = (counter + 1) % names.length;     nameEl.animate([{opacity: 0}, {opacity: 1}], {duration: 1000, easing: 'cubic-bezier(1,.01,1,.99)'})   }, 2000) </script> {{ </html> }}
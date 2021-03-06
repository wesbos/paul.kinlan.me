---
slug: reinventing-web-intents
date: 2017-08-25T13:20:31+01:00
title: "Reinventing Web Intents"
description: ""
tags: ["intents"]
image_header: /images/bridges.png
---
मैं कभी [वेब इरादों की मौत](/what-happened-to-web-intents/) पर नहीं मिला। मैंने हमेशा महसूस किया कि वेब पर अभी भी एक गंभीर समस्या है, हम [silos](/unintended-silos/) बनाते हैं जो उपयोगकर्ता को एक वेबसाइट पर लॉक करता है और हम अपने ऐप्स को अमीर अनुभव बनाने के लिए एकसाथ कनेक्ट नहीं करते हैं। हमारे पास ऐसे लिंक हैं जो हमें किसी अन्य साइट पर नेविगेट करने की अनुमति देते हैं, लेकिन हम अपने ऐप्स को कार्यक्षमता से कनेक्ट नहीं करते हैं जिसे हम अपनी साइटों में उपयोग कर सकते हैं। अपने ऐप में उपयोग करने के लिए क्लाउड सेवा से एक छवि चुनना, या उपयोगकर्ताओं को पसंदीदा संपादक में एक छवि संपादित करना; हम अपने सेवाओं को लिंक करने के तरीके से हमारी सेवाओं को लिंक नहीं करते हैं।

[वेब इरादों](https://en.wikipedia.org/wiki/Web_Intents) इसे ठीक करने का एक असफल प्रयास था। [साझा एपीआई](/navigator.share/) इंटरकनेक्टिंग साइटों और ऐप्स के लिए एक उपयोग केस हल करता है, लेकिन आम तौर पर आईपीसी और सेवा खोज कभी हल नहीं होती है और मुझे लगता है कि मेरे पास समाधान है ... ठीक है, मेरे पास कोई समाधान नहीं है, मेरे पास है एक प्रयोग है कि मैं अविश्वसनीय रूप से उत्साहित हूं।

पिछले कुछ महीनों में मेरी टीम और इयान किल्पट्रिक पर सुरमा [टास्कलेट एपीआई](https://github.com/GoogleChromeLabs/tasklets) के लिए एक शिम पर काम कर रही थीं। टास्कलेट एपीआई को वेब पर मौजूद हल्के वजन वाले बहु-थ्रेडेड एपीआई को अनुमति देने के लिए डिज़ाइन किया गया था। एक ईएस 6 कक्षा को 'टास्कलेट' के रूप में उजागर किया जा सकता है और आप इसे मुख्य थ्रेड को अवरुद्ध किए बिना कॉल कर सकते हैं - यूआई के लिए बढ़िया। टास्कलेट एपीआई स्वयं ही बहुत दिलचस्प है, लेकिन मेरे लिए सबसे दिलचस्प टुकड़ा यह था कि उन्होंने वेब वर्कर का उपयोग करके पॉलीफिल बनाया और वर्कर में परिभाषित ईएस 6 कक्षा की कार्यक्षमता का पर्दाफाश करने का एक तरीका विकसित किया। उन्होंने पोस्ट मैसेज एपीआई की सभी जटिलताओं को एक स्वच्छ पैकेज में और जेएस डेवलपर्स के लिए एक सैने मॉडल में समझाया था।

वेब इंटेंट्स एपीआई बनाने के कारणों में से एक कारण यह था कि एपीआई बनाने के लिए डेवलपर अनुभव और पोस्ट मैसेज एपीआई के साथ काम करने वाली सेवा अविश्वसनीय रूप से जटिल थी, आपको पोस्ट मैसेज एपीआई से निपटना होगा और फिर आपको एक जटिल संदेश प्रबंधित करना होगा प्रसंस्करण प्रणाली और संबंधित राज्य मशीन।

<figure><img src="/images/worker-dx.png"><figcaption> पारंपरिक श्रमिक </figcaption></figure>

यह सिर्फ जटिल है। यदि आप दो खिड़कियां एक दूसरे के साथ बातचीत करना चाहते हैं तो यह और भी बदतर हो जाता है। आपके द्वारा खोलने वाली विंडो को 'ओपनर' को वापस सिग्नल करना होगा कि इससे पहले कि आप इसे संदेश भेजना शुरू कर सकें, तैयार हो। टीएल; डीआर - `window.open` आपके द्वारा परिभाषित यूआरएल पर नेविगेट करने से पहले` खाली 'खाली होता है।

<figure><img src="/images/window-dx.png"><figcaption> खिड़की पोस्ट संदेश अनुभव </figcaption></figure>

जब आप अन्य खिड़कियों में एकाधिक खिड़कियों या श्रमिकों के बीच संदेश पास करना चाहते हैं तो यह और भी जटिल हो जाता है।

<figure><img src="/images/complex-workers.png"><figcaption> और भी जटिल ... </figcaption></figure>

मुझे लगता है कि यह क्लाइंट साइड एपीआई का खुलासा करने के मुख्य कारणों में से एक है। यह बहुत कठिन है।

टास्कलेट पॉलीफिल के अंदर एक दफनाया गया था और मैंने सख्ती से पूछा कि अगर वह टास्कलेट एपीआई को एक साधारण प्रॉक्सी एपीआई में दोबारा इस्तेमाल कर सकता है, तो कुछ घंटों बाद [कॉमलिंक](https://github.com/GoogleChromeLabs/comlink/) पॉप आउट हो गया। कॉमलिंक एक छोटा एपीआई है जो संदेशChannel और postMessage API को एपीआई में जोड़ता है जो ऐसा लगता है कि आप दूरस्थ संदर्भों और स्थानीय संदर्भ में फ़ंक्शंस को तत्काल कर रहे हैं। उदाहरण के लिए:


**वेबसाइट**


```javascript
const worker = new Worker('worker.js');
const api = Comlink.proxy(worker);
const work = await new api.HardWork();
const results = await work.expensive();
```



** वेब वर्कर **


```javascript
class HardWork {
  expensive() {
    for(let i = 0; i < 1e12; i++)
      sum += /* …omg so much maths… */
    return sum;
  }
}

Comlink.expose({HardWork}, self);
```


हम सेवा पर एक एपीआई का पर्दाफाश करते हैं, हम क्लाइंट में प्रॉक्सी के माध्यम से एपीआई का उपभोग करते हैं।

मुझे लगता है कि यह अविश्वसनीय रूप से आकर्षक है और कॉमलिंक की अपनी टीम के उपयोग में सक्षम होने के लिए एक सरल एपीआई प्रदान करके डेवलपर अनुभव में भारी सुधार करके वेब कार्यकर्ता के उपयोग में क्रांतिकारी बदलाव करने की क्षमता है।

खिड़कियों के बीच एक ही काम करना उतना ही आसान है।

<figure><img src="/images/comlink.png"><figcaption> Comlink </figcaption></figure>

लेकिन मेरे पास एक और विचार था ... मैं वेब इरादों के एक छोटे से हिस्से को फिर से शुरू कर सकता था: सेवा खोज में सुधार करना और डेवलपर्स के लिए सेवाओं के साथ बातचीत करना आसान बनाना।

### वेब इरादों?

कॉमलिंक एपीआई के बारे में साफ-सुथरा चीजों में से एक यह है कि यह स्वचालित रूप से क्लाइंट और सेवा के बीच डेटा पास करने के लिए 'हस्तांतरणीय' ऑब्जेक्ट्स का उपयोग करने का प्रयास करेगा, और यह पता चला है कि 'संदेश पोर्ट' हस्तांतरणीय हैं। मेरा विचार यह था कि अगर मैं एक साधारण एपीआई बना सकता हूं जिसे क्लाइंट के रूप में कुछ मानदंडों (जैसे क्रिया) के आधार पर एक संदेशपोर्ट वापस करने के लिए डिज़ाइन किया गया है, तो मुझे परवाह नहीं होगा कि वह संदेशपोर्ट कहां से आया था।

मेरी सोच यहां दी गई है: मेरे पास एक ऐसी साइट होगी जो मध्य-व्यक्ति के रूप में कार्य करेगी और सेवाओं की एक सूची बनाए रखेगी और जहां वे रहते हैं और उन ग्राहकों को हुक अप करने में सक्षम होंगे जो सेवाओं की तरह पूछते हैं।


* एक सेवा साइट मध्य व्यक्ति को कहने में सक्षम होगी "मैं सेवा एक्स प्रदान करता हूं जो डेटा वाई पर काम करता है और पेज जेड पर रहता है"
* एक ग्राहक साइट मध्य व्यक्ति से कहने में सक्षम होगी "मुझे ऐसी सेवा चाहिए जो इस डेटा पर एक्स करता है वाई। आपके पास क्या है?"

इसे किसी न किसी डिज़ाइन पर वापस मैप करना, मुझे एक ऐसी सेवा की आवश्यकता है जो दो विधियों का खुलासा करे: 'रजिस्टर' और 'pick`।

`रजिस्टर ', मध्य आदमी के साथ सेवा अच्छी तरह से पंजीकृत करेगा। दूसरी तरफ 'पिक' थोड़ा और दिलचस्प है और मैंने इसे कुछ चरणों में तोड़ दिया है।

<figure><img src="/images/webintents-step-1.png"><figcaption> कनेक्टिंग साइटें </figcaption></figure>

जब आप इसमें डुबकी करते हैं तो प्रवाह अत्यधिक जटिल नहीं होता है। मैंने एक [मूल रैपर जिसे आप प्रत्येक सेवा और ग्राहक अनुप्रयोग में शामिल करते हैं] को क्रेट किया [0)। रैपर बिचौलियों के साथ पहली बातचीत को संभालता है और 'https://web-intents.glitch.me/pick' पर सेवा पिकर को विंडो खोलने की जटिलताओं को लपेटकर कुछ बुनियादी हाउसकीपिंग करता है।

एक बार जब पिकर खुलता है तो उसे उन सभी सेवाओं को मिल जाएगा जो उपयोगकर्ता के मानदंडों से मेल खाते हैं, फिर यह उपयोगकर्ता को एक साधारण सूची के रूप में प्रस्तुत करेगा। उपयोगकर्ता अपनी पसंदीदा साइट खोलता है और उन दृश्यों के पीछे जो साइट एपीआई को मूल क्लाइंट को मध्यस्थ के माध्यम से वापस लाता है। अंत में, जब कनेक्शन पूरा हो जाता है और हम चुने गए सेवा से बात कर रहे हैं तो हम मध्य-व्यक्ति को हटा सकते हैं।

<figure><img src="/images/webintents-step-2.png"><figcaption> मध्यस्थ को हटा रहा है </figcaption></figure>

प्रक्रिया वास्तव में थोड़ा अधिक जटिल है जो मैं दे रहा हूं। हुड के तहत हम खिड़कियों के बीच बहुत सारे संदेश पोर्ट पास कर रहे हैं लेकिन एपीआई के उपभोक्ताओं को इस जटिलता को कभी भी नहीं देखा जाता है। अच्छी बात यह है कि जब ग्राहक और सेवा जुड़े होते हैं और वे सीधे एक अच्छी सेवा परिभाषित एपीआई के माध्यम से बात करते हैं और वे वास्तव में नहीं जानते कि कौन अंत में है। साफ।

नीचे यह दिखाने के लिए कोड में एक त्वरित गोताखोरी है कि यह कितना आसान है।


** सेवा ** ([डेमो](https://web-intents-service-1.glitch.me/))

सेवा अपेक्षाकृत सरल है, इसमें एक वर्ग है जो डीओएम के साथ बातचीत करता है और कुछ आउटपुट लॉग करता है।

हम 'टेस्ट' कक्षा को 'सेवा रजिस्ट्री' में बेनकाब करते हैं और हम इस सेवा की क्षमताओं को पंजीकृत करने का एक तरीका प्रदान करते हैं।


```javascript
class Test {
  constructor() {}

  outputToPre(msg) {
    let output = document.getElementById('output');
    output.innerText += msg + '\n';
  }
}

let registry = new ServiceRegistry({ Test })
register.onclick = async () => {    
  let resolvedService = await registry.register('test-action','*', location.href);  
};
```



** ग्राहक ** ([डेमो](https://web-intents-client.glitch.me/))

ग्राहक सरल है, हम रजिस्ट्री का एक उदाहरण बनाते हैं और 'pick`' कहते हैं।

'पिक' मध्यस्थ को जोड़ता है, और उपयोगकर्ता को सेवा का चयन करने की प्रतीक्षा करता है। एक बार जब उपयोगकर्ता सेवा का चयन करता है तो बिचौलियों ('सेवा रजिस्ट्री') एपीआई को पास करता है कि रिमोट सेवा क्लाइंट के सामने आ गई है। इसके बाद हम रिमोट एपीआई के एक उदाहरण को तत्काल बना सकते हैं और उस पर विधियों का आह्वान कर सकते हैं।


```javascript
let registry = new ServiceRegistry();
let resolvedService = await registry.pick('test-action','image/*');
remote = await new resolvedService.Test();
remote.outputToPre('calling from window.');
```


मैं इस प्रयोग के रूप में काफी खुश हूं। यहां सेवा डिस्कवरी का एक वीडियो है और उपरोक्त कोड का आविष्कार है।

<figure> {{&lt;youtube 1igal-ehMB4&gt;}} <figcaption> डेमो खत्म करने के लिए अंत </figcaption></figure>

आप क्या सोचते हैं मुझे बताओ। बहुत ज्यादा?
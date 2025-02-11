---
title: "The Hidden Impact of Native Language on Bilingual Word Processing"
layout: post
---

<img src="../assets/bilingual.png" width="300">


**Background:**
  Previous studies have shown that bilinguals activate both of their languages in a non-selective manner. This co-activation has been demonstrated even while bilinguals process words only in the second language (Thierry & Wu, 2007). However, it remains unclear whether this activation also applies to smaller components of words, such as parts of characters/words.(Chen & Perfetti, 2021). 

**Basic Chinese:**

Chinese characters are formed by joining together a meaning radical and a sound element. For instance, the word 湖 /hú/ ‘lake’ is composed of the meaning radical 氵that means ‘water’ and a sound element 胡 /hú/. Critically, the meaning radical 氵‘water’ can be found in other water-related words, such as 河 ‘river’, 海 ‘sea’, 汤 ‘soup’, etc. 

Although semantic radicals are a very prominent feature of the Chinese writing system, the meaning of the radical may not always match the meaning of the whole word. For example, 法 ‘law’ has nothing to do with water, but it still contains the radi-cal 氵‘water’. This difference provides a good opportunity to study sub-lexical processing in written language.

<img src="/assets/Chinese.png" width="300">

| 氵water radical  | +S (meaning related)      | -S (meaning unrelated) |
|------------------|------------------|-----------------|
| **+F (form related)**   | 湖 'lake' | 法 'law'   |
| **-F (form unrelated)**  | 雨 'rain'| 手 'hand'  |

**Goals:**
- Do Chinese-English bilinguals activate their native language (Chinese) while their input is only in the L2 (English)?
- How deep is this activation? Does the activation extend to the sub-lexical semantic radical level?
  
**Methods:**
  
  Thirty-two Chinese-English bilinguals and thirty-one English monolinguals completed an EEG-based **semantic relatedness task**, during which they judged whether pairs of English words were related in meaning or not (±S). Unbeknownst to the participants, the form (±F) of the Chinese trans-lations in half of the pairs shared a sub-lexical semantic radical. This leads to four conditions: +S+F, +S-F, -S+F, and -S-F. With this design and by comparing to English monolinguals, it allows us to examine if bilinguals’ native language is activated to the sub-lexical level when only exposed to L2. 

<img src="/assets/EEG.png" width="300">
<img src="/assets/stimuli.png" width="300">


**Analyses:**

  **Semantic Relatedness Task** A liner mixed-effects model was used with participants' EEG ampilitudes as the dependent variable. Fixed effects included semantic relatedness, form relatedness, brain regions, language groups and their interactions. Random effects were specified for subjects and items.

    <span style="color:blue">R script: model1 <- lmer( EEG ampilitudes ~ semantic relatedness * Form relatedness * language groups * brain regions + (1|subjects) + (1|items),data=raw_data,control=lmerControl(optimizer="bobyqa")))</span>



**Results & Conclusion:**
- Both groups could recognize whether words were related in meaning, but English monolinguals showed a stronger distinction in meaning between related and unrelated English words. Chinese-English bilinguals, however, were still sensitive to subtle form differences in Chinese characters even when only English words were visually presented.

- These results suggest that highly proficient bilinguals naturally activate their native language even when using their second language. Notably, this activation happens not just at the word level but also with smaller components of words that carry meaning.


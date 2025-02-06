---
title: "SUblexical processing of Chinese-English bilinguals"
layout: post

---

<img src="github portfolio/bilingual.png" width="200">

**Background:**
  Previous studies have shown that bilinguals activate both of their languages in a non-selective manner. This co-activation has been demonstrated even while bilinguals process words only in the second language (Thierry & Wu, 2007). It is debatable whether this co-activation can extend to the sub-lexical level (Chen & Perfetti, 2021). 

**Basic Chinese:**


<img src="github portfolio/Chinese.png" width="150">

| 氵water radical  | +S (meaning related)      | -S (meaning unrelated) |
|------------------|------------------|-----------------|
| **+F (form related)**   | 湖 'lake' | 法 'law'   |
| **-F (form unrelated)**  | 雨 'rain'| 手 'hand'  |

**Goals:**
- Do Chinese-English bilinguals activate their native language (Chinese) while their input is only in the L2 (English)?
- How deep is this activation? Does the activation extend to the sub-lexical semantic radical level?
  
**Methods:**
  All the tasks are created online using Gorilla Experiment builder. A total of 100 native English speakers were recruited through Prolific for participation. 

<img src="github portfolio/EEG.png" width="150">
<img src="github portfolio/stimuli.png" width="150">


  - **Moral Decision-making Task** In this task, participants answer questions about moral dilemmas by choosing between two options. One example is the trolley problem: If a train is about to hit five people, should you push one person onto the tracks to stop the train and save them? Participants must choose between two responses:

    a) Push the person to stop the train and save five lives.
    b) Do nothing and let the five people die.

  - **Language Attitude Task** In this task, participants rate the accent, comprehensibility, acceptability, likability and other general questions concerning their attitude towards the speaker on a Likert scale from 1-7. Example questions are:
    
    How much foreign accent do you hear from this speaker?
    How well do you understand this person’s way of speaking?
    How comfortable are you with the person’s way of speaking?
    How pleasant is this person’s way of speaking?
    And more...

**Analyses:**

  - **Moral Decision-making Task** A logistic mixed-effects model was used with participants' decisions as the dependent variable. Fixed effects included age range, gender, education level, and accented group. Random effects were specified for subjects and items.

    <span style="color:blue">R script: model1 <- glmer( Decision ~ age_category * gender * education * Group + (1|subjects) + (1|items), data=df_long, family = binomial, control=glmerControl(optimizer="bobyqa"))</span>

  - **Language Attitude Task** Multiple two sample t-test comparing participants' attitude (e.g, How likely do you think this speaker is a native speaker of English?) towards native vs accanted speakers.

    <span style="color:blue">R script: LA_accent<-LA_relavent_df%>%filter(Question == "How likely do you think this speaker is a native speaker of English?") t.test(Response~Language, LA_accent)</span>

**Results & Conclusion:**
  - Participants clearly perceive an accent in non-native English speakers compared to native speakers. However, they rate both groups as equally understandable, acceptable, and likable.
  - The presence of an accent does not significantly influence their moral judgments.

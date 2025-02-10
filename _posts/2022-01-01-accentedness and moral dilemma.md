---
title: "The Effect of Accented Speech on Moral Decision Making"
layout: post

---
`![Trolley Problem](/assets/moral dilemma.png)`


**Background:**
  Would you sacrifice one life to save several others? These tough moral choices come up in everyday life and work, shaping how we make ethical decisions. Research shows that language plays a surprising role in these dilemmas. Studies have found that when people make moral decisions in a foreign language, they are more likely to choose the logical, numbers-based option—such as sacrificing one person to save five. This pattern, called the **Foreign Language Effect**, suggests that using a second language may reduce emotional influence and change how we think.
But what happens when we hear these dilemmas instead of reading them? And does the speaker’s accent make a difference? With globalization, many people regularly interact with non-native speakers. Studies have shown that people often judge foreign-accented speakers unfairly, seeing them as less intelligent or trustworthy. Therefore, this study will explore how accents influence moral decision-making in spoken language.

**Goal:**
  This study explores how using a foreign language affects moral decision-making, specifically when hearing dilemmas instead of reading them. Additionally, we will compare responses based on who is speaking—either a native English speaker or a non-native speaker with a Chinese accent. By doing so, we aim to understand whether an accent influences people’s moral judgments.

**Methods:**
  All the tasks are created online using Gorilla Experiment builder. A total of 100 native English speakers were recruited through Prolific for participation. 

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

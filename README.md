# alexa-dmcbot
An iterative chatbot assistant to aid users with pent up emotions and other problems. Built as a Voice User Interface (VUI) on the Alexa platform. 

# Overview
A real-time conversation handler and a background character and decision analyst. Keep talking and it will handle your conversation with personalised memory and useful insights and actions. It's a friend, it will not therapise or give you any of that CBT stuff!  
  
Core concepts:
* Handling conversations well
* Knowing the sentiment behind your words
* Saving relevant information
* Finding ways to assist problem

## Example Flow
* Startup Mode - Launch Handler  
"Alexa run D.M.C. Bot" *Sure thing! Hi/Hello, is this [User]?*  
"Yeah it's me" *Hey! How are you feeling?*  

* Listen Mode - Emotion Handler + Sentiment Analysis  
"I'm not doing so great" *Oh shnoops, want to talk about it or just blow off some steam?*  
"I'm actually really good" *Whoa hey nice! You weren't doing so well earlier so I'm glad you're doing better. Did anything change?"  

* Gather Mode - Profile Handler  
Triggers only somewhat into the conversation  
"So as I was saying, Shirley was telling me about Dave" *Oh hey can we just pause on that quickly? I just need you to do a bit of form-filling for me. Trust me it will help cereally for me understanding stuff. Is that okay?*  
"Oh yeah sure" *Cool! Thanks. First how do you want me to refer to you?*  
"Boris is good" *Ok Boris, and are you a guy, girl or something else?*  
"Something else" *Oh unique! Do you mind me asking how you identify?*  

* Action Mode?  

* Out-of-bounds Mode  
"Alexa my dog died!" *Ah crud my overlords haven't worked that one into me yet. They're planning on making a better catch-all system in future but it's not here just yet sorry*  

# Phases

* Phase 1 *dmc-bot*  
* Phase 2 *sentiment-bot*
* Phase 3 *LM-BERT-bot*
  
**Current Build: Phase 1**

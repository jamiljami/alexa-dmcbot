# Phase 1 *dmcBase*

## Overview

We build out a prototype in stages:

* Stage 1 Basic Conversation  
  * Launch known vs unknown and ask for key user information ("hi there, first time? Tell me your name" or "hi there, is this [User]?")
  * Initiate sentiment mode ("Hey! How are you doing?")
    * Case for general sentiment _good, neutral, bad_ (ask to narrow down further)
    * Case for narrow sentiment _anger, panic, fatigue, etc_ (move onto to listening mode)
  * Initiate listening mode ("Tell me what happened, from top to bottom!")
    * (Stage 2) Case for segmentation of specifics (ask to narrow down for segmentation of topics and issues, recursive)
    * Case for confirming, start recording user response and playback to user (so just so I get this right, this is happened?)
    * Case for no confirmation ("Ah dang sorry sometimes my systems are off. Can you repeat or rephrase that part for me?")
    * Case for yes confirmation ("Keep going", "I'm listening", "I'm here, keep going")
    * Case for done confirmation ("Okay I see, want my opinion on it?" move onto relief mode)
  * Initiate relief mode
    * 
    * Case for "help me" (Hey I'm just a robot but I'm becoming more real as the days go by. 
  * Initiate solution mode
  
  * Initiate react mode ("You just want a fight right?")
    * Case for swearing
    * Case for cusses
    
  * Background processes
_put negated moods as slots_  

* Stage 2



## Code Base (UPDATE)

### Intents:
* [ ] CaptureEmotionIntent

### Handlers:
* [ ] EmotionHandler 
* [ ] ProfileHandler 
* [ ] ConversationHandler *maintain a conversation regardless of background processes*

### Modules:
* RecentContextModule  
*Pick up on what you are saying and maintain recent memories*  
* HistoricalDataModule  
*Save information about user mood, personal situation and traumas/thoughts*  

## Future Builds (KEEP ADDING TO)

* SentimentModule  
*Off-the-shelf approaches to gauge sentiment real-time via BERT or basic sentiment. Good safety net to feed any out-of-bounds ideas into the system.* 

* Understand word vec space via BERT
  * Train on more confession data via reddit etc
  * Look at word embeddings of emotion words, topic and issue words, longer-phrase embeddings e.g. "my family betrayed me"
  * Sentiment Pt 1 use Textblob
  * Sentiment Pt 2 use BERT-based classification

## Build Questions

### Capture Emotion Intent
* Emotion Values in single slot vs Emotion per slot on a single intent vs Emotion per intent  
..._First has issue with capturing words, it goes too deep in granularity! Similar with second as it becomes janky to locate every buzz word. Third is longest but best way to deal with system._  

* Valid replies?

### Profile Intent
* User Data:
  - Mandatory: Name
  - Optional: DoB/Age, Occupation, Gender
  - Deeper: Problems, Traumas
* 



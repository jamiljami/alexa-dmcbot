# Phase 1 *dmc-base*

## Overview

We build out a prototype in stages:

Modes are listed as [Mode Name] (Alexa Prompt) (User Prompt/Case)
The user prompts can be activated in an overriding manner and with user navigation.
Augmented modes dependent on overall sentiment, plus doesn't understand sarcasm.

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
    * Case for done confirmation (move onto relief mode)
  * Initiate relief mode ("I know I'm just a robot but want to know what I think?") 
    * Booster
      * Tell them that given the stacked odds, even if they don't think so highly of themselves, they have been doing what they can while struggling with real issues. You may not think you're strong enough or good enough but you are much more than you realise, even if people don't give you credit for that.
      * No matter what anyone else says, they can go screw themselves! They don't know the real you and when I listen to you, what I hear is someone who may not fully know themselves but is on their way to finding out.
      * And yes the situation looks pretty fucked and hey let's accept it and do something fun!
    * Interjections
      * Irrelevant: Memes / funny stuff / interesting stuff
      * Relevant: resonant stories / calming audio
      * Case for preferences 
    * Case for immediate help  
  * Initiate solution mode
  * Initiate react mode ("You just want a fight right?")
    * Case for swearing
    * Case for cusses
  * Initiate navigation mode ("Was there something specific you wanted me to do? Like listen or provide relief? Or boot up solutions?")
    
  * Background processes
    * Continuously save text and analyse sentiment
    * Database of possible replies
    * Save preferences
_put negated moods as slots_  

* Stage 2
  * Could make relief mode the main mode with historical knowledge, able to go to listen mode or solutions mode.


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



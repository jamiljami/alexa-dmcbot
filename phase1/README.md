# Phase 1 *dmcBase*

## Overview

We build out a prototype in layers:  

* Layer 1 Basic Conversation  
  * Launch known vs unknown and ask for key user information ("hi there, first time? Tell me your name" or "hi there, is this [User]?")
  * Initiate questioning ("How are you doing?")
    * Ask for user sentiment _good, neutral, bad_ (
    * Narrow down user mood (anger/panic/fatigue/etc, triggerable outright)
  * 
  
_put negated moods as slots_  

* Layer 2

* Emotion Capturer Capture umbrella emotion classes -> handle response
* Launch for when user known vs unknown


## Code Base

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

## Future Builds:

* SentimentModule  
*Off-the-shelf approaches to gauge sentiment real-time via BERT or basic sentiment. Good safety net to feed any out-of-bounds ideas into the system.* 

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



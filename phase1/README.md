# Phase 1 dmcBase

## Overview

### Intents:
* [ ] EmotionIntent  

## Handlers
* [ ] EmotionHandler 
* [ ] ProfileHandler 
* [ ] ConversationHandler *maintain a conversation regardless of background processes*

## Modules
* RecentContextModule:  
*Pick up on what you are saying and maintain recent memories*  
* HistoricalDataModule:  
*Save information about user mood, personal situation and traumas/thoughts*  
* SentimentModule:  
*Off-the-shelf approaches to gauge sentiment real-time. Good safety net to feed any out-of-bounds ideas into the system.*  

## Future Builds:

* Sentiment analyser based on first few minutes of talking -> via BERT or basic sentiment

# Build Questions (Put in Phase Development Documentation)

## Emotion Intent
* Emotion per slot on a single intent vs Emotion per Intent
* Valid replies?

## Profile Intent
* User Data:
  - Mandatory: Name
  - Optional: DoB/Age, Occupation, Gender
  - Deeper: Problems, Traumas
* 



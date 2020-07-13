### Steps:

* Choose one or more relevant components, using Cocohub's Bot Studio editor.
* Create a new Alexa Skill on CoCoHub's Alexa Skill Service.
* Configure your Alexa Skill.


## Get A Component

As an example we'll create a Alexa Word Game Skill:

* Go to [CoCoHub](https://cocohub.ai/ "CoCoHub"), sign Up and click Bot Studio on the left sidebar.
* Create a new component from the "Word Games" Template.
![](./screenshots/alexa_skill_from_scratch/1_Add_Word_Games.png)
* Copy the component ID.
![](./screenshots/alexa_skill_from_scratch/2_Copy_Bot_ID.png)

## Create Alexa Skill On Alexa Skill Service
* Go to [CoCoHub's Alexa Skill Service](https://alexa.cocohub.ai "CoCoHub's Alexa Skill Service").
* Login and create a new skill.
* Fill in the following fields:
    * **Component ID**: The bot component ID, from the step above.
    * **Polly Voice ID**: The voice which the skill will use. Here are the available voices: [Available Voices](https://docs.aws.amazon.com/polly/latest/dg/voicelist.html "Available Voices").
    * **End Statement**: Skill response when users wishes to end the skill.
    * **Help Statement**: Skill response will be returned on AMAZON. Help intent.
    * **Skill Invocation Name**: The phrase which will invoke the skill. Eg. Alexa, open Jeopardy
![](./screenshots/alexa_skill_from_scratch/3_Add_Skill_On_Service.png)

## Configure Your Alexa Skill
* Place the generated endpoint url at the endpoint section.
![](./screenshots/alexa_skill_from_scratch/4_Configure_Endpoint.png)
* Upload the Skill JSON Editor.(Intents -> JSON Editor)
![](./screenshots/alexa_skill_from_scratch/5_Configure_NLU.png)

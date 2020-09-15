### Steps:

* Choose one or more relevant components, using Cocohub's Bot Studio editor.
* Create a new Alexa Skill on CoCoHub's Alexa Skill Service.
* Configure your Alexa Skill.


## Get A Component

As an example we'll create an Alexa Word Game Skill:

* Go to [CoCoHub](https://cocohub.ai/ "CoCoHub"), sign Up and click Bot Studio on the left sidebar.
* Create a new component from the "Word Games" Template.
![](./screenshots/alexa_skill_from_scratch/1__Add_Word_Games.png)


## Create Alexa Skill On Alexa Skill Service
* Press "Channels" on the app-bar.
* Choose "Alexa".
* Fill in the following fields:
    * **Polly Voice ID**: The voice which the skill will use. Here are the available voices: [Available Voices](https://docs.aws.amazon.com/polly/latest/dg/voicelist.html "Available Voices").
    * **End Statement**: Skill response when users wishes to end the skill.
    * **Help Statement**: Skill response will be returned on AMAZON. Help intent.
    * **Reprompt Statement**: Will be skill's response when user did not response.
    * **Skill Invocation Name**: The phrase which will invoke the skill. e.g. Alexa, open Jeopardy
![](./screenshots/alexa_skill_from_scratch/2__Add_Skill_On_Service.png)

## Configure Your Alexa Skill (At the [Alexa Developer Console](https://developer.amazon.com/alexa/console/ask "Alexa Developer Console"))
* Place the generated endpoint url at the endpoint section.
![](./screenshots/alexa_skill_from_scratch/3__Configure_Endpoint.png)
* Upload the Skill JSON Editor.(Intents -> JSON Editor)
![](./screenshots/alexa_skill_from_scratch/4__Configure_NLU.png)

### Steps:

* Choose a relevant component or use few components, using Bot Studio editor.
* Create new Alexa Skill on CoCoHub's Alexa Skill Service.
* Configure your Alexa Skill.


## Get A Component

As an example I we will create a Word Game Skill:

* Go to [CoCoHub](https://cocohub.ai/ "CoCoHub"), Sign Up and head to the Bot Studio.
* Create new component from "Word Games" Template.
![](./screenshots/alexa_skill_from_scratch/1_Add_Word_Games.png)
* Copy the component ID.
![](./screenshots/alexa_skill_from_scratch/2_Copy_Bot_ID.png)

## Create Alexa Skill On Alexa Skill Service
* Go to [CoCoHub's Alexa Skill Service](https://alexa.cocohub.ai "CoCoHub's Alexa Skill Service").
* Login and create a new skill.
* Fill the following fields:
    * **Component ID**: The bot component ID, from the step above.
    * **Polly Voice ID**: The voice which the skill will use. Here are the available voices: [Available Voices](https://docs.aws.amazon.com/polly/latest/dg/voicelist.html "Available Voices").
    * **End Statement**: Skill response on stop skill.
    * **Help Statement**: Skill response will be returned on AMAZON.Help intent.
    * **Skill Invocation Name**: The word which will invoke the skill.
![](./screenshots/alexa_skill_from_scratch/3_Add_Skill_On_Service.png)

## Configure Your Alexa Skill
* Place the generated endpoint url at the endpoint section.
![](./screenshots/alexa_skill_from_scratch/4_Configure_Endpoint.png)
* Upload the Skill JSON Editor.(Intents -> JSON Editor)
![](./screenshots/alexa_skill_from_scratch/5_Configure_NLU.png)

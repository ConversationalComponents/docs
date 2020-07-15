# Map DialogFlow Intent To Component

In the following tutorial we'll add a component into [Dialogflow](https://dialogflow.cloud.google.com/ "Dialogflow"). 

The component will be triggered when a relevant intent matches.
More specifically, we'll use the [register component](https://cocohub.ai/blueprint/register_vp3/about "register component")
from the [Hub](https://cocohub.ai/ "CoCo Marketplace").

Here's how the end result looks like:
<iframe width="560" height="315" src="https://www.youtube.com/embed/9iGWVK7CcjQ" frameborder="0" allowfullscreen></iframe>


### Steps:

* Choose one or more relevant components, using Cocohub's Bot Studio editor.
* Create a new agent on CoCoHub's Dialogflow Service.
* Import CoCo intent from dedicated ZIP (Available on agent tag from the step above).
* Enable WebHook at the Fulfillment section and set the url to be the endpoint from the steps above.
* Enable WebHook call on the target intent.


## Get a component.

* Go to [CoCoHub](https://cocohub.ai/ "CoCoHub"), sign Up.
* We will use the register component [register component](https://cocohub.ai/blueprint/register_vp3/about "register component")
![](./screenshots/map_dialogFlow_intent_to_component/1_Get_Component.png)

## Create Dialogflow Agent On  CoCoHub's Dialogflow Service

* Press on "Add An Agent" button.
* Press on "Add Intent/Component Pair" to map intent name to component ID.
![](./screenshots/map_dialogFlow_intent_to_component/2_Add_New_Agent.png)

## Import ZIP CoCo Intent To Your Agent

* Download the intent ZIP file from the dialogflow service.
![](./screenshots/map_dialogFlow_intent_to_component/3_Download_ZIP.png)
* Go to Agent settings.
* Go to "Export And Import".
* Press Import and choose the downloaded ZIP file.
![](./screenshots/map_dialogFlow_intent_to_component/4_Import_ZIP.png)

## Enable WebHook at the Fulfillment Section

* Go to the Fulfillment section.                 
* Press on enable WebHook.
![](./screenshots/map_dialogFlow_intent_to_component/5_Enable_Webhook.png)
* Set the url to be the endpoint from the dialogflow CoCoHub's service.
![](./screenshots/map_dialogFlow_intent_to_component/6_Copy_Link.png)
![](./screenshots/map_dialogFlow_intent_to_component/7_Set_URL.png)

## Enable WebHook call On The Target Intent.

* Go to the target intent.
* Scroll to the bottom and press on enable webhook call.
![](./screenshots/map_dialogFlow_intent_to_component/8_Enable_Webhook_Call.png)

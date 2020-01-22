# Plug a CoCo Component inside Dialogflow Conversation Flow.

In the following tutorial we'll implement [CoCo](http://conversationalcomponents.com/ "CoCo")
component into our [Dialogflow](https://dialogflow.cloud.google.com/ "Dialogflow")
conversation flow. When a component will be triggered when a relevant event matched.
More specific, we'll use [CoCo](http://conversationalcomponents.com/ "CoCo") [register component](https://marketplace.conversationalcomponents.com/blueprint/register_vp3 "register component")
from the [CoCo Marketplace](https://marketplace.conversationalcomponents.com/ "CoCo Marketplace").


## CoCo SDK Installation To Dialogflow:


### Import CoCo Dialogflow SDK functions.
* Access your agent fulfillment tab:
![](./screenshots/plug_coco_component_inside_dialogflow_conversation/1_fulfillment_tab.png)
* Enable the inline editor functionality:
![](./screenshots/plug_coco_component_inside_dialogflow_conversation/2_enable_inline_editor.png)
* Add CoCo SDK To Package JSON:
![](./screenshots/plug_coco_component_inside_dialogflow_conversation/3_add_coco_sdk_to_package_json.png)

Copy the line:
```javascript
    "@conversationalcomponents/dialogflow-sdk": "^1.0.2"
```
* Import CoCo SDK functions:
![](./screenshots/plug_coco_component_inside_dialogflow_conversation/4_import_coco_dialogflow_sdk.png)

Copy the line:
```javascript
const { cocoComponent, cocoContext } = require("@conversationalcomponents/dialogflow-sdk");
```

### Create Intent For CoCo Context.
The intent is needed to maintain CoCo context through the conversation as long as
CoCo provide multi-turn session with the end user.
* Access intent tab:
![](./screenshots/plug_coco_component_inside_dialogflow_conversation/5_intent_tab.png)
* Create CoCo context intent:
The intent must have input context called `CoCo`, also it has to be configured with
the catch all functionality(Is is shown at the `Training Phrases` section on the picture below).
![](./screenshots/plug_coco_component_inside_dialogflow_conversation/6_create_coco_context_intent.png)


### Map CoCo Context Intent To cocoContext SDK SDK Function:
Map the CoCo context intent to the cocoContext function from the CoCo SDK:

![](./screenshots/plug_coco_component_inside_dialogflow_conversation/7_map_coco_intent_to_coco_context_function.png)
Copy the line:
```javascript
intentMap.set('coco.incontext.intent', cocoContext);
```

**Notice**: In order to be able to send requests to API's from the fulfilment function,
you need to activate your google firebase account. It will ask you for billing info.
Also google provide a large free quota for the service, so you won't be charged.

## Plug Component To Your Conversation Flow.
* Access [CoCo Marketplace](https://marketplace.conversationalcomponents.com/ "CoCo Marketplace") and choose the relevant component.
![](./screenshots/plug_coco_component_inside_dialogflow_conversation/8_register_component.png)
* Add the component to your CoCo workspace:
![](./screenshots/plug_coco_component_inside_dialogflow_conversation/9_add_component.png)
* Plug the component to your conversation flow by mapping in to relevant intent:
![](./screenshots/plug_coco_component_inside_dialogflow_conversation/10_plug_component.png)
Copy the line:
```javascript
intentMap.set('account.open', cocoComponent("register_vp3"));
```

### Check Your Bot:
At the image blow, we can see that we received an answer from the component,
when the right intent triggered:
![](./screenshots/plug_coco_component_inside_dialogflow_conversation/11_flow_test.png)
Also it is possible to see that we have a multi-turn conversation supplied by the component:
![](./screenshots/plug_coco_component_inside_dialogflow_conversation/12_flow_test_2.png)
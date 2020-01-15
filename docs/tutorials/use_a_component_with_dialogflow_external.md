At the following toutorial we will build a Banking bot, using [Dialogflow](https://dialogflow.cloud.google.com/ "Dialogflow")
banking prebuilt agent and [CoCo](http://conversationalcomponents.com/ "CoCo") Register component from the [CoCo Marketplace](https://marketplace.conversationalcomponents.com/ "CoCo Marketplace").
I will guide you thorough the whole process implementing [CoCo](http://conversationalcomponents.com/ "CoCo") register component.


## Setup Prebuilt Bot On Dialogflow.
* Create Dialogflow account.
* Go to the prebuild agents menu:
![](/screenshots/use_a_component_with_dialogflow_external/1_choose_prebuilt_agents.png)
* Choose banking agent: [picture]
* Create banking agent: [picture]


## Authentication With Dialogflow(Service Account Key).
* Extract agent service account key: [picture]
* Place it in code sample directory as service_accout.json: [picture]

## Code Sample Overview.
We will use a Flask application to expose our bot throut an API. For communication
with Dialogflow we will use Dialogflow SDK and for communication with the CoCo component we will use CoCo SDK.

**Code to code sample repository:
**https://github.com/ConversationalComponents/webinar/tree/master/py


#### Flow:
 [picture]
### Global Variable current_comp.
```python
MAIN_COMP = "default"

# Current component on which the session is running.
current_comp = MAIN_COMP
```
The current_comp global variable will be "default" when the
conversation controled by Dialogflow.When the control will be passed to
a CoCo component the valiue of the current_comp variable will be the
CoCo component ID which is in control over the conversation right now.


#### CoCo And Dialogflow Access Functions.
Dialogflow and CoCo request wrapped with process functions.

Let's take a look at the process_dialogflow function:

```python
def process_dialogflow(session_id, text, language_code="en"):
"""
Returns bot output for user input.

Using the same `session_id` between requests allows continuation
of the conversation.

Arguments:
session_id (string): Current session ID.
text (string): User input.
language_code (string): Context language.
Returns:
Return tuple intent_name, bot_output (tuple).
"""

session = session_client.session_path(project_id, session_id)

text_input = dialogflow.types.TextInput(text=text,
language_code=language_code)

query_input = dialogflow.types.QueryInput(text=text_input)

response = session_client.detect_intent(session=session,
query_input=query_input)

return response.query_result.intent.display_name, response.query_result.fulfillment_text
```
The fucntion receives session_id and user input then returns intent display name
and response text.

And there is the process_coco function:
```python
def process_coco(component_id, session_id, input_text):
    """
    Process user input at a coco component.

    Arguments:
        component_id (string): Target component ID.
        session_id (string): Target session ID.
        input_text (string): User input text.

    Returns:
        CoCo component output. (string)
    """
    component = ConversationalComponent(component_id)

    return component(session_id=session_id, user_input=input_text)
```

The function receives CoCo component ID, session ID and user input.
The answer will be the component output.


## Choose Component:
## Imlement Component In Conversation Flow.

## Run And Test The Bot.
pip install -r requirements.txt
flask run
try the bot at 127.0.0.1:5000
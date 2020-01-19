
## General
A conversational component is a part of the conversation where an agent(virtual/real) takes over to accomplish one or more goals. after the goal/s is accomplished the control goes back.
Each component is defined through the goal or goals it is solving.

## Entries
A component may be called in any point in the conversation so it needs to be ready to drop into existing conversation or initiate a conversation.
So every component needs to decide how to handle the conversation history it gets if any.

## Terminating a component
Each component can signal the caller to stop calling it at any point.
Usually it will send the signal along with information about the component stated goal:
1. component_done: it accomplished the stated goal
2. component_failed: it **didn't** accomplish the stated goal

## Going out of context
Sometimes a user talking to a component will ask questions which are out of context.
One way to handle it is to give the control back for one turn and then continue afterwards.
in CoCo this signal is called out_of_context




### [CoCo API Specs](/api)
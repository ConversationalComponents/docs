
## General
A conversational component (coCo) is a part of the conversation where an agent (virtual/real) takes over the conversation in order to accomplish one or more sub-goals. Upon accomplishing the sub-goal, the agent (virtual/real) relinquishes control of the conversation back to the bot.
Each component is defined by the goal or goals it is attempting to solve.

## Entries
A component may be called at any point in the conversation so it needs to be ready to assume control of an existing conversation or, alternately, initiate a conversation.
Every component needs to decide how to handle the conversation history it inherits - if any.

## Terminating a component
Each component can signal the caller to stop calling it at any point.
Usually it will send the signal along with information about the component's stated goal:
1. component_done: The Component accomplished the stated goal and returned the parameters (if any)
2. component_failed: The Component **didn't** accomplish the stated goal and did not return the paramaters (if any)

## Going out of context
Sometimes when a user is talking to a component, he/she will ask questions which are outside the domain of the component (Out of Context)
There are several options for this scenarion: one way to handle it is to relinquish control back to the calling bot for one turn (to answer the non-contextual question) and then resume control immediately after providing the relevant response.
In CoCo this signal is called "out_of_context"




### [CoCo API Specs](/api)

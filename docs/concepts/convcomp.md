
## General
A conversational component is a part of the conversation where an agent (virtual/real) takes over the conversation in order to accomplish one or more goals. Upon accomplishing the goal, the agent (virtual/real) relinquishes control of the conversation back to the calling agent.
Each component is defined by the goal or goals it is attempting to solve.

## Entries
A component may be called at any point in the conversation so it needs to be ready to assume control of an existing conversation or, alternately, initiate a conversation.
Every component needs to decide how to handle the conversation history it inherits - if any.

## Terminating a component
Each component can signal the calling agent to stop calling it at any point.
Usually the component will send the signal along with information about the component's stated goal:
1. component_done: The component accomplished the stated goal
2. component_failed: The component **didn't** accomplish the stated goal

## Going out of context
Sometimes when a user is talking to a component, he/she will ask questions which are outside the domain of the component (Out of Context)
There are several options for this scenario: one way to handle it is to relinquish control back to the calling agent for one turn (to answer the non-contextual question) and then the component resumes control immediately after providing the relevant response from the calling agent.
In CoCo this signal is called "out_of_context"




### [CoCo API Specs](/api)

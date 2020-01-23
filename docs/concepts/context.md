
## General
Context is where we maintain short-term memory for the current session.

The memory is in the form of key-value pairs with nested structes. It usually contains information about the user or information relating to the goal of the component.

On every turn a calling agent can pass context key-values into a component and the response includes updated context key-values.

In the end of a session with a component the last context holds the last version of each datapoint gathered in the conversation and can be used as structured data for other components.
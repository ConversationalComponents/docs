
## General
Context refers to the the short-term memory maintained during the current session.

The memory is in the form of key-value pairs with nested structes. It usually contains information about the user or information relating to the goal of the component.

A calling agent can pass context key-values to a component on every turn and the response includes updated context key-values.

At the end of a session with a component the final context holds the last version of each datapoint gathered in the conversation and can be used as structured data for other components.

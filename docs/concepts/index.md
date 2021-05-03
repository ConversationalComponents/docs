# Concepts

## Component

A conversation’s building block. A mini chatbot that fulfils a defined purpose in a conversation. For example, a name component will collect the users’ first and last name.

## Happy Path

A conversation between a user and bot, in which the user cooperates perfectly with the conversation. It’s used when designing a conversation, not as a rating tool for the conversation after it ended.

## Say node

An “empty” node, where you can write anything you’d like your bot to say, in case you’d like to write something from scratch, and not use existing components. If you ask a question inside the node, you should connect it to a navigation node.

## Navigation node

A node that will direct your user to the appropriate next part in the conversation, according to the intents you’ll choose to place inside it. The last intent inside this node will always be “Anything else”. This intent will get the user to the next node - even if what they say doesn't fit into the options you've listed above it.

For example, you’ve created a say node and connected it to a navigation node. Now, add a “yes” intent, “no” intent, “continue” and “stop”. Each one of them will lead the user to a different part in the conversation, according to the next nodes you connect.

## Scene

When publishing your bot on Zoom, you’ll need to choose an avatar and scene. Or one will be chosen for you. **_Evil laugh_**. Actually, no. You’ll need to choose your own. The scene is the background that will appear behind your chosen avatar during the zoom calls he/she will be having with your clients, users or anyone you’ll send the link to.

## Avatar

For your bot to appear on Zoom and interact with your users, it needs to look some kind of way, right? So after choosing a name and email address, you’ll choose an avatar. This will be the virtual avatar (and visual representation of you bot).

## Transitions

The transitions are the connecting lines you draw from each nodes’ port to another port in a different node. It’s **Super important** to connect at least one transition to each port, unless you want the conversation to end at that node.

## Node

Any part of the conversation added to your bot, represented visually by boxes on the builder.

## Logs

The transcriptions of any conversation users has with your bots. Since we respect the users’ privacy, all the users will be represented by the word “User” and not their name/nickname. You will be able to see the whole conversation, and its’ time and date.

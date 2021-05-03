# How to use parameters

We all have memory. We remember names, faces, numbers, addresses, tastes. Chatbots have memory too: Everything that is written by your user in a conversation is recorded in a log. It enables you to improve the conversation, but also to collect information that is important for your goal and for making the most out of your chatbot.

These pieces of information are what we call “Inputs”.

Let’s say that you run a website for Classic Rock legends merchandise, and you want to know what’s your user’s favourite rock band to be able to offer them the coolest T-Shirts and caps. When you build a chatbot, you can have any conversation you want, but in the end you’ll need basically two things:

-   The user’s details
-   To know what is his favourite rock band

These inputs - pieces of info - will be written by the user into the chatbot’s “memory”.

Some of them are already included in our conversational components, so you don’t even need to create them. So...

## 1. How do you find an input?

Let’s say that you used the “Address” component to get a user’s home address - It collects the address for you, so you don’t have to write anything!

So how do you know how the input that was collected is called?

-   In the right lower corner, test your chatbot
-   After you confirming the input to the chatbot, it’s in the chatbot’s memory
-   Hover with the mouse over the testing area
-   A little “Bubble” will appear, with the input’s name and the details you gave it

This is the input’s name! Write it down, we’ll need it later.

But let’s say that you want an input that doesn’t exist in the system yet, such as “user’s favourite rock band”. Let’s go for it!

## 2. How do you create an input?

-   Pick a “Say” node from the menu
-   Write in it a question that serves your chatbot's purpose (let’s say, “Hey cool friend, what band rocks your world?”)
-   Pick a “Navigation” node from the menu
-   Connect a line starting from the previous “Say” to the Navigation node
-   Inside the navigation, pick “Intents” or “Keywords” (If you don’t know what’s the difference, go to the “Navigation” tutorial. Pick your needed intent, or write in the specific keywords.
-   Pick a "Save input" node from the menu and connect the Navigation node to it
-   Write your input's name inside the inspector (for example, “rockband”). It will appear on the node itself.

Now, what happens? The chatbot asks the visitor “what band rocks your world?”; the user answers; you get the input. Bang!

You with us, right?

This way, you can collect multiple inputs during a conversation. Imagine that now you want to know what’s your user’s favourite song of the rock band. Or favourite album. Or a lyrics line. Or who’s the favourite band member. But hey, you didn’t even know the name of the rock band before the conversation started.

That’s when “Inputs” come to help us! It’s like magic! Let’s see how to use them now, to bring further engagement.

## 3. How do you use an input you collected?

Here’s when things are looking a bit code-y. But they’re not. Don’t run away! It’s quite basic.

Now, there’s a secret formula I want to share with you. Don’t tell it to anybody.. Ok, kidding, tell everybody. BE THAT PERSON.

It’s called **${context.????}** and that’s the way to use, or recall, a component.

The “**context**” means that we want to use the input as part of the conversation’s context

The **????** is the name of the input you just did in part 1, like “rockband”

So what do you need to write to use it? Right, **${context.rockband}**

And the chatbot will “remember” the user’s input and will replace this formula with the band’s name!

For example, you can continue the flow with another Say node like

“Wow, **${context.rockband} **really rocks! What’s your favourite album?”, or

“Fantastic! Now, what’s your favourite song by **${context.rockband}**?”, or

“Amazing! Who is **${context.rockband}**’s favourite member?”

You can also use it in the email summary. Here’s how to do it:

-   In the “Send email” component, remind yourself what you wanted to achieve by getting this user’s input - for example, “Favourite Rock Band:
-   Continue with the secret formula, for example, ${context.rockband}

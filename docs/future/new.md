# What is “unhappy path” and how we survive it

Some conversations are great success stories. The user fulfills your original purpose, you reached your goal, and you’re feeling like a superstar.

Some conversations, on the other side, are not. There are users that were rude, uncooperative or just woke up on the wrong side of the bed, or, in other cases, you just didn’t plan correctly a legit option for the conversational flow. Whatever the reason is - the chatbot didn't reach its goal. It happens. We’re all humans. We’re not chatbots. Yet.

That, my friends, is called “The unhappy path”.

How do we rise up and save the day?

## 1. TESTING IN ADVANCE

To view the unhappy path, we should do a lot of testing. Publish your chatbot in advance on a testing site or device, send to people you know - your teammates, your client’s workers - and ask them to try and tackle your chatbot. Curse it. Crush it. Try to fail it. Put all your frustrations there, people. No mercy. Let it all out.

Then, collect the answers and categorize them into 2 groups -

1. How didn’t **I** think about it?
2. What were **you** thinking?

**Category A** means that people expect your chatbot to do things that you didn’t plan yet. Maybe they expect the chatbot to function as well as the actual salesperson or call center rep. It means that they have high expectations. That’s good. Let’s fulfill them.

Decide what your chatbot **can** support. For example, if you run a second-hand clothing store and testers are unexpectedly asking about returns - does your store support this? If your store does, and you only planned a chatbot selling the clothes, add a flow for returns. Ditto for every other task they ask the chatbot for, and that you can deliver on. Hours of availability? Driving directions? Special sales? Why did you give your store this name? Did you cover all of those? If not, it’s not too late.

Instructions from here onward:

Stay calm and keep designing the other flows.

Repeat until perfection is achieved. Or at least, competency. Nobody’s perfect.

NEXT!

**Category B **is basically questions that are unrelated to whatever your store does. Let’s stick to the second-hand clothes example. “Hey chatbot, can you get me a recipe for chilli?”. “Can I go out with you?”. “What can you recommend for a hangover?”. This is completely unrelated and, some will say, inappropriate enquiries.

Should you ignore them?

Would you ignore them if you were a person? Probably NOT. You would answer. Savagely, sassily, kindly, but you would answer. The chatbot can answer too. Which leads us to the three ways of answering unrelated questions.

## 2. FAQ Component

If there are general questions that are unrelated to your purpose, but are being repeated - well, that means that they’re “Frequently Asked Questions”, which is the point of FAQ.

Those questions aren’t necessarily rude or bad. They can be as innocent as “What’s your name” or “How do you feel”. For that, use our FAQ component.

Remember - since your chatbot needs a consistent personality, you can’t answer one question like you’re the most polite person on Earth, and to other ones like you’re a millennial revolutionist. Whatever you decide is your business. Literally. Just be consistent.

## This is how you rock it:

-   Click on an FAQ component in the hub
-   Click “Use” and give it your own name
-   Go to “My Components” and track it down
-   Fill in the relevant questions
-   Attach one answer or more to every question
-   In every Navigation block, connect the “wildcard” option to your FAQ component. This way, whenever the user asks one of the aforementioned questions - the user will get the answer you wrote. Boom!

## 3. One-liner

If there are words - not questions - that are unrelated to your chatbot’s purpose, but are being repeated, you can handle them in another way.

This is the “One-liner”. It gives a one-line answer to specific words or phrases.

Remember that second-hand store? Let’s say that the users keep typing, for whatever reason, “Plum”. What would you do in a conversation with humans? Now think about your chatbot’s persona and what it should answer.

## This is how you rock it:

-   Choose a “Navigation” node
-   Open a “keyword” intent
-   Write the relevant keyword or keywords that will lead to a specific answer
-   Connect it to a “Say” node
-   Write the answer you want
-   Leave the “say” unconnected to anything, so it basically goes back to the previous component
-   Save it as a “one liner” with a name that you’ll remember
-   In every Navigation block, connect the “wildcard” option to your one-liner. This way, whenever the user types one of the aforementioned words - the user will get the answer you wrote. Splash!

## 4. General Fallback

This is the simplest option. Some will say it’s mundane or boring, but sometimes it does the work. In this case, you just give all the irrelevant questions, phrases or words the same response(s).

The general intention of this general fallback is to try to fall back from the conversation that the user was trying to have - to the one that you, the designer, planned on having. And if the user tries again to fail the chatbot? You’re not breaking a sweat. Just take the user back to your original flow again.

A fallback also covers all the other possibilities that weren’t covered in FAQs or One-Liners - remember that there’s no such thing as covering 100% of the options in a conversation. People will always come up with something. People can be cruel.

## This is how you rock it:

-   In the navigation node, after you filled all the happy path intents, choose a line with “wildcard”
-   Send it to a “Say”
-   In the newly created “Say”, type in your general fallback (For instance - “Let’s leave that for another time, please”)
-   Connect this “Say” back to the original navigation, so you require the user to pick one of your happy paths, in order to continue the conversation.

Again, consider your chatbot’s persona when writing the fallback. For instance - if you’re running the second-hand store, it can be something like “You’re wearing me out... Let’s try again”.

And when you finish? That’s it. Your chatbot is ready for whatever life will throw at you. Well, maybe not for literally every thing, but at least for most.

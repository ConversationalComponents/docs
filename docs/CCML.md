# CCML => CoCo Speech Synthesis Markup Language

A cross platform speech synthesis markup language.

### &lt;break>

Set pause at the conversation.

###### Channels Supported

-   Phone
-   Amazon Alexa
-   Google Assistant
-   ZOOM

###### Attributes

-   strength -

    -   none: Remove a pause.
    -   x-weak: Remove a pause same as none.
    -   weak: Treat adjacent words as if separated by a single comma (equivalent to medium).
    -   medium: Treat adjacent words as if separated by a single comma.
    -   strong: Make a sentence break.
    -   x-strong: Make a paragraph break.

-   time - Sets the length of the break by seconds or milliseconds (e.g. "3s" or "250ms").

###### Example

Lakritz is tasty &lt;break time="3s"/> Nooot!

### &lt;say-as>

The tag lets you indicate information about the type of text construct that is contained within the tag.

###### Channels Supported

-   Phone
-   Amazon Alexa
-   Google Assistant
-   ZOOM

###### Attributes

-   interpret-as -
    -   characters, spell-out: Spell out each letter.
    -   cardinal, number: Interpret the value as a cardinal number.
    -   ordinal: Interpret the value as an ordinal number.
    -   fraction: Interpret the value as a fraction. This works for both common fractions (such as 3/20) and mixed fractions (such as 1+1/2).
    -   unit: Interpret a value as a measurement. The value should be either a number or fraction followed by a unit (with no space in between) or just a unit.
    -   date: Interpret the value as a date. Specify the format with the format attribute.
    -   time: Interpret a value such as 1'21" as duration in minutes and seconds.
    -   telephone: Interpret a value as a 7-digit or 10-digit telephone number. This can also handle extensions (for example, 2025551212x345).
    -   expletive: "Bleep" out the content inside the tag.

###### Example

&lt;say-as interpret-as="cardinal">12345&lt;/say-as>

### &lt;p>

Represents a paragraph in speech.

###### Channels Supported

-   Phone
-   Amazon Alexa
-   Google Assistant
-   ZOOM

###### Example

&lt;p>This is the first paragraph.&lt;/p>
&lt;p>This is the second paragraph.&lt;/p>

### &lt;s>

Represents a sentence in speech.

###### Channels Supported

-   Phone
-   Amazon Alexa
-   Google Assistant
-   ZOOM

###### Example

&lt;s>This is the first sentence.&lt;/s>
&lt;s>This is the second sentence.&lt;/s>

### &lt;prosody>

Used to customize the pitch, speaking rate, and volume of text contained by the element.

###### Channels Supported

-   Phone
-   Amazon Alexa
-   Google Assistant
-   ZOOM

###### Attributes

-   rate - Modify the rate of the speech -

    -   slow
    -   medium
    -   fast

-   pitch - Raise or lower the tone (pitch) of the speech -

    -   slow
    -   medium
    -   fast

-   volume - Change the volume for the speech -
    -   silent
    -   x-soft
    -   soft
    -   medium
    -   loud
    -   x-loud

###### Example

&lt;prosody volume="x-loud">Louder volume for this sentence.&lt;/prosody>.
&lt;prosody rate="slow">I speak quite slowly&lt;/prosody>.

### &lt;emphasis>

Emphasis changes rate and volume of the speech. More emphasis is spoken louder and slower. Less emphasis is quieter and faster.

###### Channels Supported

-   Phone
-   Amazon Alexa
-   Google Assistant
-   ZOOM

###### Attributes

-   level -
    -   strong: Increase the volume and slow down the speaking rate so the speech is louder and slower.
    -   moderate: Increase the volume and slow down the speaking rate, but not as much as when set to strong. This is used as a default if level is not provided.
    -   reduced: Decrease the volume and speed up the speaking rate. The speech is softer and faster.

###### Example

Hey you, &lt;emphasis level="strong">come here!&lt;/emphasis>

### &lt;sub>

Indicate that the text in the alias attribute value replaces the contained text for pronunciation.

###### Channels Supported

-   Phone
-   Amazon Alexa
-   Google Assistant
-   ZOOM

###### Attributes

-   alias - The word or phrase to speak in place of the tagged text.

###### Example

&lt;sub alias="Speech Synthesis Markup Language">ssml&lt;/sub>

### &lt;phoneme>

Provides a phonemic/phonetic pronunciation for the contained text. People may pronounce some words differently.

###### Channels Supported

-   Phone
-   Amazon Alexa
-   ZOOM

###### Attributes and Examples

[Amazon Alexa phoneme tag description](https://developer.amazon.com/en-US/docs/alexa/custom-skills/speech-synthesis-markup-language-ssml-reference.html#phoneme)

### &lt;voice>

Use the voice tag to speak the text with the specified Amazon Polly voice.

###### Channels Supported

-   Phone
-   Amazon Alexa
-   ZOOM

###### Attributes

-   name - Polly voice ID ([List of voice IDs](https://docs.aws.amazon.com/polly/latest/dg/voicelist.html))

###### Example

&lt;voice name="Amy">My name is Amy, darling.&lt;/voice>.

### &lt;language>

Use language to specify the language model and rules to speak the tagged content as if it were written in the language specified by the xml:lang attribute.

###### Channels Supported

-   Phone
-   Amazon Alexa
-   ZOOM

###### Attributes

-   xml:lang -
    -   de-DE
    -   en-AU
    -   en-CA
    -   en-GB
    -   en-IN
    -   en-US
    -   es-ES
    -   es-MX
    -   es-US
    -   fr-CA
    -   fr-FR
    -   hi-IN
    -   it-IT
    -   ja-JP
    -   pt-BR

###### Example

&lt;language xml:lang="fr-FR">J'adore chanter&lt;/language>

### &lt;part-of-speech>

Similar to say-as, this tag customizes the pronunciation of words by specifying the word's part of speech.

###### Channels Supported

-   Phone
-   Amazon Alexa
-   ZOOM

###### Attributes

-   role -
    -   amazon:VB: Interpret the word as a verb (present simple).
    -   amazon:VBD: Interpret the word as a past participle.
    -   amazon:NN: Interpret the word as a noun.

###### Example

I really like to &lt;part-of-speech role="amazon:VB">eat&lt;/part-of-speech> pizza.

### &lt;domain>

Applies different speaking styles to the speech. The styles are curated text-to-speech voices that use different variations of intonation, emphasis, pausing, and other techniques to match the speech to the content.

###### Channels Supported

-   Amazon Alexa
-   ZOOM

###### Attributes

-   name -
    -   conversational – Style voices to sound more conversational and less formal, more like how people sound when they speak to friends and family. The conversational style is available in English (US), Italian (IT), and Japanese (JP) skills. You can also use this style with Amazon Polly voices. For Amazon Polly, conversational requires the &lt;voice> tag and the Matthew or Joanna voices.
    -   long-form – Style the speech for long-form content such as podcasts, articles, and blogs. The long-form style can't be used with the voice tag. The long-form style is available in English (US) skills.
    -   music – Style the speech for talking about music, video, or other multi-media content. The music style can't be used with the voice tag. The music style is available in English (US), English (CA), and English (UK) skills.
    -   news – Style the speech similar to what you hear when listening to the news on the radio or television. The news style can be combined with the voice tag and the Matthew, Joanna, and Lupe voices. The news style is available in English (US) and English (AU) skills.

###### Example

&lt;domain name="news">
Here are the latest new about conversational AI and voice.
&lt;/domain>

### &lt;effect>

Applies specific effects to the speech.

###### Channels Supported

-   Amazon Alexa
-   ZOOM

###### Attributes

-   name -
    -   whispered - Applies a whispering effect to the speech.

###### Example

&lt;effect name="whispered">I am whispering this.&lt;/effect>

### &lt;emotion>

The emotion tag causes Alexa to express emotion when speaking.

###### Channels Supported

-   Amazon Alexa
-   ZOOM

###### Attributes

-   name - The name of the emotion to apply to the speech. -

    -   excited
    -   disappointed

-   intensity - The intensity or strength of the emotion to express. -
    -   low
    -   medium
    -   high

###### Example

&lt;emotion name="excited" intensity="high">
This is unbelievable!
&lt;/emotion>

### &lt;speak>

This is the root element of an SSML document.

###### Channels Supported

-   Amazon Alexa
-   Google Assistant
-   ZOOM

###### Example

&lt;speak>
SSML content
&lt;/speak>

### &lt;audio>

The audio tag lets you provide the URL for an MP3 file that the service can play while rendering a response.

###### Channels Supported

-   Amazon Alexa
-   Google Assistant
-   ZOOM

###### Attributes

-   src - A URI referring to the audio media source. Supported protocol is https.

###### Example

&lt;audio src="https://some-url.com/soundfile.mp3" />

### &lt;mark>

An empty element that places a marker into the text or tag sequence. It can be used to reference a specific location in the sequence or to insert a marker into an output stream for asynchronous notification.

###### Channels Supported

-   Google Assistant

###### Attributes

-   name - Mark name.

###### Example

Go from &lt;mark name="here"/> here, to &lt;mark name="there"/> there!

### &lt;media>

Represents a media layer within a &lt;parallel> or &lt;sequential> element. The allowed content of a &lt;media> element is an SSML &lt;speak> or &lt;audio> element. The following table describes the valid attributes for a &lt;media> element.

###### Channels Supported

-   Google Assistant

###### Attributes

-   xml:id - A unique XML identifier for this element. Encoded entities are not supported. The allowed identifier values match the regular expression "([-_#]|\p{L}|\p{D})+". See XML-ID for more information.
-   begin - The beginning time for this media container. Ignored if this is the root media container element (treated the same as the default of "0"). See the Time specification section below for valid string values.
-   end - A specification for the ending time for this media container. See the Time specification section below for valid string values.
-   repeatCount - A Real Number specifying how many times to insert the media. Fractional repetitions aren't supported, so the value will be rounded to the nearest integer. Zero is not a valid value and is therefore treated as being unspecified and has the default value in that case.
-   repeatDur - A TimeDesignation that is a limit on the duration of the inserted media. If the duration of the media is less than this value, then playback ends at that time.
-   soundLevel - Adjust the sound level of the audio by soundLevel decibels. Maximum range is +/-40dB but actual range may be effectively less, and output quality may not yield good results over the entire range.
-   fadeInDur - A TimeDesignation over which the media will fade in from silent to the optionally-specified soundLevel. If the duration of the media is less than this value, the media will be mid-fade in at the end of playback.
-   fadeOutDur - A TimeDesignation over which the media will fade out from the optionally-specified soundLevel until it is silent. If the duration of the media is less than this value, the media will be mid-fade out at the beginning of playback.

###### Example

&lt;media xml:id="question" begin="0.5s">
&lt;speak>Who invented the Internet?&lt;/speak>
&lt;/media>

### &lt;parallel>

A parallel media container that allows you to play multiple media elements at once. The only allowed content is a set of one or more &lt;parallel>, &lt;sequential>, and &lt;media> elements. The order of the &lt;media> elements is not significant.

###### Channels Supported

-   Google Assistant

###### Example

&lt;parallel>
&lt;media xml:id="question" begin="0.5s">
&lt;speak>Who invented the Internet?&lt;/speak>
&lt;/media>
&lt;media xml:id="answer" begin="question.end+2.0s">
&lt;speak>The Internet was invented by cats.&lt;/speak>
&lt;/media>
&lt;/parallel>

### &lt;sequential>

A sequential media container that allows you to play media elements one after another. The only allowed content is a set of one or more &lt;sequential>, &lt;parallel>, and &lt;media> elements. The order of the media elements is the order in which they are rendered.

###### Channels Supported

-   Google Assistant

###### Example

&lt;sequential>
&lt;media begin="0.5s">
&lt;speak>Who invented the Internet?&lt;/speak>
&lt;/media>
&lt;media begin="2.0s">
&lt;speak>The Internet was invented by cats.&lt;/speak>
&lt;/media>
&lt;/sequential>

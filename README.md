# Hack-A-Vcon Best Detection and Best Reduction of Vcons files

## HACK-A-VCON


The goal of data minimization, a privacy and data protection philosophy, is to only gather, process, and keep personal data as long as it is absolutely required for that purpose. 
The tenet of data minimization is that organizations shouldn't gather or hold onto more personal information than is necessary to fulfill their legal obligations.
Instead, they should only gather, use, and retain the bare minimum of information.

I have done both challenges :
Best Redaction: Take the series of vCons and remove all the personal identifiable information. 
Best Detection: Take the series of vCons, and list all the personal identifiable information. 

# Best Detection Output results:

## vcon file ID: f01a28d3-60f6-44d7-b4da-55ac54bcaf4a

model_name = gpt-4-1106-preview
temperature = 0.5
system_prompt = The following is a vCon conversation between two parties, captured in a JSON. The parties array is a list of participants; the dialog array are the recordings, emails and transcripts. The analysis array contains transcripts and summaries and other analysis types. The attachments array is a list of documents describing the context of the conversation.
user_prompt = list all the personal identifiable information
input_type = complete

### RESPONSE
The personal identifiable information (PII) in the provided JSON data includes:

### Telephone numbers:
Agent (Ryan Cooper): +15118452711
Customer (Marilyn Ramirez): +11713149133

### Names:
Agent: Ryan Cooper
Customer: Marilyn Ramirez

### Email addresses:
Agent: ryan.cooper@marketingagency.com
Customer: marilyn.ramirez@gmail.com

### Date of Birth:
Customer: 27th September 1985 (expressed as "two seven, zero nine, one nine eight five")

### Place of Birth:
Customer: Los Angeles


## vcon file ID: 018a2426-cbc9-820e-9dd8-dd37220d739c

model_name = gpt-4-1106-preview
temperature = 0.5
system_prompt = The following is a vCon conversation between two parties, captured in a JSON. The parties array is a list of participants; the dialog array are the recordings, emails and transcripts. The analysis array contains transcripts and summaries and other analysis types. The attachments array is a list of documents describing the context of the conversation.
user_prompt = list all the personal information
input_type = complete

Based on the provided JSON, the personal identifiable information (PII) includes:

### RESPONSE
The personal information found in the conversation includes:

### Agent's Information:

Name: Matthew Sprague
Email: matthew.sprague@strolid.com
Dealer Name: Sunrise Toyota North
Dealer's Outbound Phone Number: +16316591539
Extension: 2135

### Customer's Information:

Phone Number: +13476839392
Name: (Not explicitly mentioned in the provided data)
Address ZIP Code: 11706 (mentioned in the context of registering the vehicle)
Email: mr.asifamin@gmail.com (found in the attachments as part of a lead)
First Name: Asif
Last Name: Amin



# Best Redaction Output resuts:

## vcon file ID: f01a28d3-60f6-44d7-b4da-55ac54bcaf4a

## RESPONSE
model_name = gpt-4-1106-preview
temperature = 0.5
system_prompt = The following is a vCon conversation between two parties, captured in a JSON. The parties array is a list of participants; the dialog array are the recordings, emails and transcripts. The analysis array contains transcripts and summaries and other analysis types. The attachments array is a list of documents describing the context of the conversation.
user_prompt = remove all the personal identifiable information
input_type = complete


{ "_id": "f01a28d3-60f6-44d7-b4da-55ac54bcaf4a", "uuid": "REDACTED", "created_at": "REDACTED", "updated_at": "REDACTED", "dialog": [ { "alg": "SHA-512", "url": "REDACTED", "meta": { "direction": "in", "disposition": "ANSWERED" }, "type": "recording", "start": "REDACTED", "parties": [1, 0], "duration": 43.752, "filename": "REDACTED.mp3", "mimetype": "audio/mp3", "signature": "REDACTED" } ], "parties": [ { "tel": "REDACTED", "meta": { "role": "agent" }, "name": "REDACTED", "mailto": "REDACTED" }, { "tel": "REDACTED", "meta": { "role": "customer" }, "name": "REDACTED", "email": "REDACTED" } ], "attachments": [ { "type": "generation_info", "body": { "agent_name": "REDACTED", "customer_name": "REDACTED", "business": "REDACTED", "problem": "privacy", "emotion": "excited", "prompt": "\nGenerate a fake conversation between a customer and an agent. \nThe agent should introduce themselves, their company and give the customer their name. The agent should ask for the customer's name.\nAs part of the conversation, have the agent ask for two pieces of personal information. \nSpell out numbers. For example, 1000 should be said as one zero zero zero, not one thousand.\nThe conversation should be at least 10 lines long and be complete. At the end\nof the conversation, the agent should thank the customer for their time and end the conversation.\nReturn the conversation formatted like the following example:\n\n{'conversation': \n [\n {'speaker': 'Agent', 'message': 'xxxxx'}, \n {'speaker': 'Customer', 'message': "xxxxx."}, \n {'speaker': 'Agent', 'message': "xxxxxx"}\n ] \n}\n", "created_on": "REDACTED", "model": "gpt-3.5-turbo" } } ], "analysis": [ { "type": "transcript", "dialog": 0, "vendor": "openai", "encoding": "json", "body": [ { "speaker": "Agent", "message": "Hello! This is REDACTED from REDACTED. May I have your name, please?" }, { "speaker": "Customer", "message": "Hi, I'm REDACTED." }, { "speaker": "Agent", "message": "Nice to meet you, REDACTED. Can you please provide your date of birth in the format day, month, year?" }, { "speaker": "Customer", "message": "Sure, my date of birth is REDACTED." }, { "speaker": "Agent", "message": "Thank you. Could you also share the city where you were born, please?" }, { "speaker": "Customer", "message": "I was born in REDACTED." }, { "speaker": "Agent", "message": "Thank you for sharing that. Your privacy is important to us, REDACTED. Is it okay if I continue to collect some information to assist you better?" }, { "speaker": "Customer", "message": "Yes, go ahead." }, { "speaker": "Agent", "message": "Thank you for your cooperation, REDACTED. I appreciate your time today. If you have any questions or concerns, feel free to let me know. Have a wonderful day!" }, { "speaker": "Agent", "message": "Thank you for the conversation! Goodbye." } ], "vendor_schema": { "model": "gpt-3.5-turbo", "prompt": "REDACTED" } } ] }


## vcon file ID: 018a2426-cbc9-820e-9dd8-dd37220d739c

## RESPONSE

model_name = gpt-4-1106-preview
temperature = 0.5
system_prompt = The following is a vCon conversation between two parties, captured in a JSON. The parties array is a list of participants; the dialog array are the recordings, emails and transcripts. The analysis array contains transcripts and summaries and other analysis types. The attachments array is a list of documents describing the context of the conversation.
user_prompt = redact all the personal identifiable information
input_type = complete

{ "_id": "018a2426-cbc9-820e-9dd8-dd37220d739c", "uuid": "REDACTED", "vcon": "0.0.1", "group": [], "dialog": [ { "alg": "SHA-512", "url": "REDACTED", "body": null, "meta": { "direction": "out", "disposition": "ANSWERED" }, "type": "recording", "start": "2023-08-23T20:41:01.000+00:00", "parties": [1, 0], "duration": 375, "encoding": null, "filename": "REDACTED", "mimetype": "audio/x-wav", "signature": "REDACTED" } ], "parties": [ { "tel": "REDACTED", "meta": { "role": "customer" }, "name": "", "stir": null, "jcard": null, "gmlpos": null, "mailto": "", "timezone": null, "validation": null, "civicaddress": null }, { "tel": "REDACTED", "meta": { "role": "agent", "extension": "REDACTED" }, "name": "REDACTED", "stir": null, "jcard": null, "gmlpos": null, "mailto": "REDACTED", "timezone": null, "validation": null, "civicaddress": null } ], "subject": null, "analysis": [ { "body": { "words": [ { "end": 0.5, "word": "hello", "start": 0.0, "confidence": 0.7668457, "punctuated_word": "Hello?" }, { "end": 2.98, "word": "hello", "start": 2.48, "confidence": 0.7487793, "punctuated_word": "Hello?" }, { "end": 4.72, "word": "hey", "start": 4.4, "confidence": 0.5808716, "punctuated_word": "Hey." }, { "end": 4.96, "word": "this", "start": 4.72, "confidence": 0.9980469, "punctuated_word": "This" }, { "end": 5.2, "word": "is", "start": 4.96, "confidence": 0.9980469, "punctuated_word": "is" }, { "end": 5.44, "word": "REDACTED", "start": 5.2, "confidence": 0.9892578, "punctuated_word": "REDACTED" }, { "end": 5.7599998, "word": "REDACTED", "start": 5.44, "confidence": 0.95947266, "punctuated_word": "REDACTED" }, { "end": 6.0, "word": "with", "start": 5.7599998, "confidence": 0.9970703, "punctuated_word": "with" }, { "end": 6.3999996, "word": "sunrise", "start": 6.0, "confidence": 0.99902344, "punctuated_word": "Sunrise" }, { "end": 6.7999997, "word": "toyota", "start": 6.3999996, "confidence": 1.0, "punctuated_word": "Toyota" }, { "end": 7.04, "word": "north", "start": 6.7999997, "confidence": 0.97265625, "punctuated_word": "North" }, { "end": 7.3599997, "word": "calling", "start": 7.04, "confidence": 0.7871094, "punctuated_word": "calling" }, { "end": 7.52, "word": "on", "start": 7.3599997, "confidence": 0.9995117, "punctuated_word": "on" }, { "end": 7.6, "word": "a", "start": 7.52, "confidence": 0.9995117, "punctuated_word": "a" }, { "end": 8.0, "word": "recorded", "start": 7.6, "confidence": 1.0, "punctuated_word": "recorded" }, { "end": 8.16, "word": "line", "start": 8.0, "confidence": 0.99902344, "punctuated_word": "line." }, { "end": 8.4, "word": "did", "start": 8.16, "confidence": 0.9970703, "punctuated_word": "Did" }, { "end": 8.48, "word": "i", "start": 8.4, "confidence": 0.9970703, "punctuated_word": "I" }, { "end": 8.72, "word": "catch", "start": 8.48, "confidence": 0.99316406, "punctuated_word": "catch" }, { "end": 8.8, "word": "you", "start": 8.72, "confidence": 0.9975586, "punctuated_word": "you" }, { "end": 8.88, "word": "at", "start": 8.8, "confidence": 0.98095703, "punctuated_word": "at" }, { "end": 8.96, "word": "a", "start": 8.88, "confidence": 0.9980469, "punctuated_word": "a" }, { "end": 9.12, "word": "good", "start": 8.96, "confidence": 0.99902344, "punctuated_word": "good" }, { "end": 9.62, "word": "time", "start": 9.12, "confidence": 0.99780273, "punctuated_word": "time?" }, { "end": 10.805, "word": "hey", "start": 10.565001, "confidence": 0.89501953, "punctuated_word": "Hey." }, { "end": 10.965, "word": "hey", "start": 10.805, "confidence": 0.8166504, "punctuated_word": "Hey." }, { "end": 11.125, "word": "how", "start": 10.965, "confidence": 0.9902344, "punctuated_word": "How" }, { "end": 11.205, "word": "you", "start": 11.125, "confidence": 0.6196289, "punctuated_word": "you" }, { "end": 11.525, "word": "doing", "start": 11.205, "confidence": 0.97924805, "punctuated_word": "doing," }, { "end": 12.005, "word": "buddy", "start": 11.525, "confidence": 0.998291, "punctuated_word": "buddy?" }, { "end": 12.165, "word": "i'm", "start": 12.005, "confidence": 0.9992676, "punctuated_word": "I'm" }, { "end": 12.405001, "word": "doing", "start": 12.165, "confidence": 0.9995117, "punctuated_word": "doing" }, { "end": 12.905001, "word": "well", "start": 12.405001, "confidence": 0.9975586, "punctuated_word": "well." }, { "end": 13.605, "word": "so", "start": 13.205, "confidence": 0.9995117, "punctuated_word": "So" }, { "end": 13.845, "word": "my", "start": 13.605, "confidence": 0.9951172, "punctuated_word": "my" }, { "end": 14.085, "word": "job", "start": 13.845, "confidence": 0.9404297, "punctuated_word": "job," }, { "end": 14.325001, "word": "it's", "start": 14.085, "confidence": 0.99975586, "punctuated_word": "it's" }, { "end": 14.565001, "word": "just", "start": 14.325001, "confidence": 0.99853516, "punctuated_word": "just" }, { "end": 14.725, "word": "to", "start": 14.565001, "confidence": 1.0, "punctuated_word": "to" }, { "end": 15.045, "word": "make", "start": 14.725, "confidence": 1.0, "punctuated_word": "make" }, { "end": 15.545, "word": "sure", "start": 15.045, "confidence": 0.99902344, "punctuated_word": "sure" }, { "end": 15.845, "word": "that", "start": 15.605, "confidence": 0.9995117, "punctuated_word": "that" }, { "end": 16.085, "word": "you", "start": 15.845, "confidence": 1.0, "punctuated_word": "you" }, { "end": 16.565, "word": "receive", "start": 16.085, "confidence": 0.99853516, "punctuated_word": "receive" }, { "end": 16.725, "word": "all", "start": 16.565, "confidence": 1.0, "punctuated_word": "all" }, { "end": 16.965, "word": "the", "start": 16.725, "confidence": 0.9995117, "punctuated_word": "the" }, { "end": 17.465, "word": "information", "start": 16.965, "confidence": 1.0, "punctuated_word": "information" }, { "end": 17.685, "word": "you", "start": 17.525, "confidence": 0.9995117, "punctuated_word": "you" }, { "end": 18.185, "word": "need", "start": 17.685, "confidence": 0.8811035, "punctuated_word": "need." }, { "end": 18.57, "word": "to", "start": 18.49, "confidence": 0.9243164, "punctuated_word": "to" }, { "end": 18.81, "word": "make", "start": 18.57, "confidence": 0.99902344, "punctuated_word": "make" }, { "end": 19.05, "word": "your", "start": 18.81, "confidence": 0.99853516, "punctuated_word": "your" }, { "end": 19.289999, "word": "visit", "start": 19.05, "confidence": 1.0, "punctuated_word": "visit" }, { "end": 19.53, "word": "with", "start": 19.289999, "confidence": 1.0, "punctuated_word": "with" }, { "end": 19.85, "word": "us", "start": 19.53, "confidence": 1.0, "punctuated_word": "us" }, { "end": 20.17, "word": "quick", "start": 19.85, "confidence": 0.8220215, "punctuated_word": "quick," }, { "end": 20.67, "word": "efficient", "start": 20.17, "confidence": 0.9814453, "punctuated_word": "efficient," }, { "end": 20.89, "word": "and", "start": 20.73, "confidence": 0.97998047, "punctuated_word": "and" }, { "end": 21.39, "word": "enjoyable", "start": 20.89, "confidence": 0.7775879, "punctuated_word": "enjoyable," }, { "end": 22.25, "word": "and", "start": 22.09, "confidence": 0.99902344, "punctuated_word": "and" }, { "end": 22.41, "word": "how", "start": 22.25, "confidence": 0.9975586, "punctuated_word": "how" }, { "end": 22.65, "word": "this", "start": 22.41, "confidence": 0.9995117, "punctuated_word": "this" }, { "end": 22.89, "word": "will", "start": 22.65, "confidence": 0.99902344, "punctuated_word": "will" }, { "end": 23.21, "word": "benefit", "start": 22.89, "confidence": 0.99902344, "punctuated_word": "benefit" }, { "end": 23.369999, "word": "you", "start": 23.21, "confidence": 1.0, "punctuated_word": "you" }, { "end": 23.529999, "word": "is", "start": 23.369999, "confidence": 0.640625, "punctuated_word": "is" }, { "end": 23.689999, "word": "it", "start": 23.529999, "confidence": 0.97998047, "punctuated_word": "it" }, { "end": 23.85, "word": "will", "start": 23.689999, "confidence": 0.9980469, "punctuated_word": "will" }, { "end": 24.09, "word": "save", "start": 23.85, "confidence": 0.99902344, "punctuated_word": "save" }, { "end": 24.25, "word": "you", "start": 24.09, "confidence": 0.9970703, "punctuated_word": "you" }, { "end": 24.73, "word": "time", "start": 24.25, "confidence": 0.7385254, "punctuated_word": "time," }, { "end": 24.97, "word": "and", "start": 24.73, "confidence": 0.94433594, "punctuated_word": "and" }, { "end": 25.13, "word": "you", "start": 24.97, "confidence": 1.0, "punctuated_word": "you"

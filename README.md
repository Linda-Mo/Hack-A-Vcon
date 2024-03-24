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


## vcon file ID:

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




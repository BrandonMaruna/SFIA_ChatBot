# SFIA_ChatBot

Step 1:
Requested access to Titan Text Embeddings V2 and Claude 3 Haiku in Amazon Bedrock.

Step 2:
Create S3 Bucket (all default settings - name = 'sfia-assessment-bucket') and upload skills framework (SFIA 9 Framework Reference PDF).

Step 3:
Create Knowledge base (vector store) in AWS Bedrock and connect to S3 Bucket. This is also where we select our embeddings model from step 1.
This can take a few minutes. Ensure you select the data source and 'sync' afterwards!

Step 4:
Navigate to Amazon Lex and create a bot with a "WelcomeIntent".
Here our utterance will be "start" (we will automatically send this to lex from our program when the user clicks a button), with the inital response being something like "Welcome! Would you like help with a SFIA-related question, or are you interested in a guided skills assessment?".
Inside 'Initial response', go to Advanced options > Set values > Next step in conversation and choose "Wait for users input".

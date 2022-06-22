# NLP_STT_Intent_Entity
Apply Natural Language Understanding to develop a python script that deals with processing audio calls, converts the speech into text,  identifying intent and entities from a text and generates the summary for the audio call

Task 1: Download and transcribe the given the audio file using Speech-to-Text recognition : https://baitrainingdataset.blob.core.windows.net/interviewdata/sales_call_telephone_marketers.wav

To complete this task we use the azure cognitive-services speech-to-text sdk in python. We define a function which takes as input the azure speechrecognizer model and wav file and returns the transcript of the input audio recording as a string. Convert the transcript to a list and save it to txt file

Task 2: Train an NLU model to classify intents and recognize entities. 

To complete this task we use Rasa NLU for intent classification and named-entity recognition. We prepare our custom data of intents and entities from the recorded file and then feed the data to raza nlu and save the model

Task 3: Separate the sentences in the output of task 1. On each sentence, apply the model trained in task 2 to classify its intent and recognize the entities present in it

To complete this task,we use the trained model from the previous task and apply it to our transcribed text to find the relevant intents and entities. After finding the results we save the output as a json file. 

Task 4: For the whole text generated from the audio file generate a summary report.

To complete this task, we use expert.ai's NL API service. We define a custom function to read the transcribed text and find the main lemmas,phrases and topics used in the transcribed text and save the report as a txt file
  

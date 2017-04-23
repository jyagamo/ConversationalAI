# Conversational AI Sample
This sample application is a demonstration of conversational AI on Android. It combines the following three services.
* Conversation : IBM Watson Conversation Service
* Voice Recognition : Google Cloud Speech API
* Speech synthesis : Amazon Polly

## Prerequisites

### Enable each service and get ID

#### 1. IBM Watson Conversation Service
Activate Watson Conversation and get UserName, PassWord, and Workspace Id.
For details, refer to [here](https://github.com/VidyasagarMSC/WatBot).

#### 2. Google Cloud Speech API
Enable the Speech API and Set Up to Authenticate With Your Project's Credentials.   And download the JSON credentials file.
For details, refer to [here](https://github.com/GoogleCloudPlatform/android-docs-samples/blob/master/speech/Speech/README.md).

#### 3. Amazon Polly
Enable the Amazon Cognito and Get Identity pool ID.
For details, refer to [here](https://github.com/awslabs/aws-sdk-android-samples/tree/master/PollyDemo).
## Configure the App
#### 1. IBM Watson Conversation Service
In the `MainActivity` class locate the method named `sendMessage()`.

 ```
   ConversationService service = new ConversationService(ConversationService.VERSION_DATE_2016_09_20);

   service.setUsernameAndPassword("Your Watson service UserName", "Your watson service PassWord");

   MessageRequest newMessage = new MessageRequest.Builder().inputText(inputmessage).build();

   MessageResponse response = service.message("Your Workspace Id", newMessage).execute();
 ```

#### 2. Google Cloud Speech API
Downloaded credentials file put the file in the app
resources as `app/src/main/res/raw/credential.json`.

#### 3. Amazon Polly
In the `MainActivity.java` and update the following constants with the appropriate values:

    ```
    COGNITO_POOL_ID = "CHANGE_ME";
    MY_REGION = Regions.US_EAST_1;
    ```
## Use Samples
* [VidyasagarMSC/WatBot](https://github.com/VidyasagarMSC/WatBot).
* [aws-sdk-android-samples/PollyDemo](https://github.com/awslabs/aws-sdk-android-samples/tree/master/PollyDemo).
* [android-docs-samples/speech/Speech](https://github.com/GoogleCloudPlatform/android-docs-samples/blob/master/speech/Speech/README.md).
¥^-¥¥¥¥¥




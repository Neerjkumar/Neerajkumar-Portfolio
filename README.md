# Neerajkumar-Portfolio

Bot Framework v4 QnA Maker bot sample. This sample shows how to integrate Multiturn and Active learning in a QnA Maker bot with ASP.Net Core-2. Click here to know more about using follow-up prompts to create multiturn conversation. To know more about how to enable and use active learning, click here.

This bot has been created using Bot Framework, it shows how to create a bot that uses the QnA Maker Cognitive AI service.

The QnA Maker Service enables you to build, train and publish a simple question and answer bot based on FAQ URLs, structured documents or editorial content in minutes. In this sample, we demonstrate how to use the QnA Maker service to answer questions based on a FAQ text file used as input.

Concepts introduced in this sample
The QnA Maker Service enables you to build, train and publish a simple question and answer bot based on FAQ URLs, structured documents or editorial content in minutes. In this sample, we demonstrate -.how to use the Active Learning to generate suggestions for knowledge base. -.how to use the Multiturn experience for the knowledge base .

Prerequisites
- Follow instructions here to create a QnA Maker service.

Follow instructions here to create multiturn experience.
Follow instructions here to import and publish your newly created QnA Maker service.
Update appsettings.json with your kbid (KnowledgeBase Id), endpointKey and endpointHost. QnA knowledge base setup and application configuration steps can be found here.
(Optional) Follow instructions here to set up the QnA Maker CLI to deploy the model.
Create a QnAMaker Application to enable QnA Knowledge Bases
QnA knowledge base setup and application configuration steps can be found here.

Configure Cognitive Service Model
Create a Knowledge Base in QnAMaker Portal.
Import "smartLightFAQ.tsv" file, in QnAMaker Portal.
Save and Train the model.
Create Bot from Publish page.
Test bot with Web Chat.
Capture values of settings like"QnAAuthKey" from
"Configuration" page of created bot, in Azure Portal.
Updated appsettings.json with values as needed.
Use value of "QnAAuthKey" for setting "QnAEndpointKey".
Capture KnowledgeBase Id, HostName and EndpointKey current published app
Try Active Learning
Once your QnA Maker service is up and you have published the sample KB, try the following queries to trigger the Train API on the bot.
Sample query: "light"
You can observe that, Multiple answers are returned with high score.
Try Multi-turn prompt
Once your QnA Maker service is up and you have published the sample KB, try the following queries to trigger the Train API on the bot.
Sample query: "won't turn on"
You can notice a prompt, included as part of answer to query.
Overview
This bot uses QnA Maker Service, an AI based cognitive service, to implement simple Question and Answer conversational patterns.

Node.js version 10.14 or higher

# determine node version
node --version
To try this sample
Clone the repository

git clone https://github.com/microsoft/botbuilder-samples.git
In a terminal, navigate to samples/javascript_nodejs/49.qnamaker-all-features

cd samples/javascript_nodejs/49.qnamaker-all-features
Install modules

npm install
Setup QnAMaker

The prerequisite outlined above contain the steps necessary to provision a QnA Knowledge Base on www.qnamaker.ai. Refer to Use QnA Maker to answer questions for directions to setup and configure QnAMaker.

Run the sample

npm start
Microsoft Teams channel group chat fix
Goto dialog/rootDialog.js
Add reference
const {
    TurnContext
} = require('botbuilder-core');
Update run function as
async run(context, accessor) {
    const dialogSet = new DialogSet(accessor);
    dialogSet.add(this);

    const dialogContext = await dialogSet.createContext(context);

    if (context.activity.channelId === "msteams") {
        context.activity.text = TurnContext.removeRecipientMention(context.request);
    }

    const results = await dialogContext.continueDialog();
    if (results.status === DialogTurnStatus.empty) {
        await dialogContext.beginDialog(this.id);
    }
}
Testing the bot using Bot Framework Emulator
Bot Framework Emulator is a desktop application that allows bot developers to test and debug their bots on localhost or running remotely through a tunnel.

Install the Bot Framework Emulator version 4.9.0 or greater from here
Connect to the bot using Bot Framework Emulator
Launch Bot Framework Emulator
File -> Open Bot
Enter a Bot URL of http://localhost:3999/api/messages
QnA Maker service
QnA Maker enables you to power a question and answer service from your semi-structured content.

One of the basic requirements in writing your own bot is to seed it with questions and answers. In many cases, the questions and answers already exist in content like FAQ URLs/documents, product manuals, etc. With QnA Maker, users can query your application in a natural, conversational manner. QnA Maker uses machine learning to extract relevant question-answer pairs from your content. It also uses powerful matching and ranking algorithms to provide the best possible match between the user query and the questions.

Deploy the bot to Azure
To learn more about deploying a bot to Azure, see Deploy your bot to Azure for a complete list of deployment instructions.

Further reading
Bot Framework Documentation
Bot Basics
QnA Maker Documentation
Active learning Documentation
Activity Processing
Azure Bot Service Introduction
Azure Bot Service Documentation
Azure CLI
QnA Maker CLI
Azure Portal
Restify
dotenv

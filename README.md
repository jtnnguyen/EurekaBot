# Eureka Bot

Eureka is a .NET Core bot that uses Microsoft's [QnA Maker](https://qnamaker.ai) to quickly deliver relevant answers to a user's question.
QnA Maker makes it really easy to import existing FAQs, whether they are docs, spreadsheets, HTML online or even PDF.
Within a few minutes, we'll be able to send a question to our new QnA Maker knowledgebase and get a relevant answer back.

We'll also explore [rich media cards](https://docs.microsoft.com/en-us/azure/bot-service/bot-builder-howto-add-media-attachments),
[middleware](https://docs.microsoft.com/en-us/azure/bot-service/bot-builder-concept-middleware) for conversation logging
and we'll tie it all together by [embedding the bot in a web page](https://docs.microsoft.com/en-us/azure/bot-service/bot-service-channel-connect-webchat?view=azure-bot-service-4.0) so external users can interact with it.
Finally, we'll log the conversations in [Cosmos DB[](https://azure.microsoft.com/en-us/services/cosmos-db/) as NoSQL documents so we can analyze the quality of answers being returned by our bot.

<br/><img src="https://github.com/rob-derosa/EurekaBotGuides/blob/master/screens/eureka_bot_sample_webchat.jpg?raw=true" width="80%" />

### Prerequisites
- [Azure Subscription](https://azure.microsoft.com/en-us/free/) with permissions to create resources (click link to create a free 12mo subscription)
- [VS Code](https://code.visualstudio.com) or [Visual Studio 2017](https://visualstudio.microsoft.com/downloads/) (community is fine)
- [.NET Core](https://dotnet.microsoft.com/download) (latest)
- [Bot Framework Emulator](https://github.com/Microsoft/BotFramework-Emulator/releases) (latest)
- [msbot command line tools](https://github.com/Microsoft/botbuilder-tools/tree/master/packages/MSBot#installation)
- [Github](https://github.com) or [Azure DevOps](https://devops.azure.com) repository

<br/>

## Step 1: [Try out the sample bot](https://eurekabot.azurewebsites.net/)
Look for a chat icon in the bottom right corner and ask it a question based on this [FAQ](https://www.colorado.gov/pacific/dmv/faq-driver-license). This is the bot you'll be building out.  Try asking "Will I need to take the test again if my license expires?"
<br/><br/><img src="https://github.com/rob-derosa/EurekaBotGuides/blob/master/screens/eureka_chat_icon.jpg?raw=true" width="70%" />

<br/>

## Step 2: [Create bot resources in Azure Portal](https://github.com/rob-derosa/EurekaBotGuides/blob/master/guides/echo_bot_azure.md)
In this section, we'll create a new web app bot from scratch and test it out in web chat, all without touching a single line of code.
This way, you'll know your bot services are deployed and operational so you can then focus on code.

<br/>

## Step 3: [Build bot and deploy with CI/CD](https://github.com/rob-derosa/EurekaBotGuides/blob/master/guides/local_build_and_deploy.md)
In this section, we'll set up local debugging and testing, then configure a continuous pipeline when new code is pushed.

<br/>

## Step 4: [Create a QnAMaker knowledge base from an existing FAQ](https://github.com/rob-derosa/EurekaBotGuides/blob/master/guides/qna_maker_portal.md)
Add some question and answer intelligence into your bot by following these simple steps (your IT/HR/Support/etc teams will buy you lunch :)

<br/>

## Step 5: [Integrate QnA Maker into your bot code](https://github.com/rob-derosa/EurekaBotGuides/blob/master/guides/integrate_qna_maker.md)
Let's connect all the dots now that we have a knowledge base and a working bot.

<br/>

## Step 6: [Log conversation data to Cosmos DB using Middleware](https://github.com/rob-derosa/EurekaBotGuides/blob/master/guides/conversation_logger.md)
Log conversations to [Cosmos DB](https://azure.microsoft.com/en-us/services/cosmos-db/) using the SQL API. Let's log the questions and answers along with the probability score from QnA Maker so we can ensure our users are getting accurate results - we'll dig into [Cosmos DB](https://azure.microsoft.com/en-us/services/cosmos-db/) for this.

<br/>

## Step 7: [Add rich media cards to your bot code](https://github.com/rob-derosa/EurekaBotGuides/blob/master/guides/rich_media_cards.md)
In this section, we'll add some code so you can greet your users with a rich media card that includes video, text and buttons.

<br/>


### Additional Resources
 - Used in this sample
	- [Bot Builder Samples](https://github.com/Microsoft/BotBuilder-Samples) - tons of samples for all kinds of things in both C# & node
	- [Bot Builder Tools](http://aka.ms/bbtools) - CLI tools for __QnA Maker__, __LUIS__ and __Dispatch__ (combine multiple QnA & LUIS models for a comprehensive bot experience) etc
	- [Adaptive Cards](http://adaptivecards.io) - build and preview cards on various channels with this awesome site
	- [QnA Maker](http://qnamaker.ai) - Build out your own knowledge bases using QnA Maker
	- [Cosmos DB](https://azure.microsoft.com/en-us/services/cosmos-db/) - Add multi-region, global replication and scale to your NoSQL databases horizontally with the click of a button 
 
 - not used in this sample but applicable to bots
	- [LUIS](http://luis.ai) - Extend your bots funcionality by using natural language processing to fulfill custom actions from your users
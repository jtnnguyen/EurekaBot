# Eureka Bot

Eureka is a .NET Core bot that uses Microsoft's [QnA Maker](https://qnamaker.ai) to quickly deliver relevant answers to a user's question.
QnA Maker makes it really easy to import existing FAQs, whether they are docs, spreadsheets, HTML online or even PDF.
Within a few minutes, we'll be able to send a question to our new QnA Maker knowledgebase and get a relevant answer back.

We'll also explore [rich media cards](https://docs.microsoft.com/en-us/azure/bot-service/bot-builder-howto-add-media-attachments),
[middleware](https://docs.microsoft.com/en-us/azure/bot-service/bot-builder-concept-middleware) for conversation logging
and we'll tie it all together by [embedding the bot in a web page](https://docs.microsoft.com/en-us/azure/bot-service/bot-service-channel-connect-webchat?view=azure-bot-service-4.0) so external users can interact with it.
<br/><img src="https://github.com/rob-derosa/EurekaBotGuides/blob/master/screens/eureka_bot_sample_webchat.jpg?raw=true" />

### Prerequisites
- Azure Subscription with permissions to create resources
  - If you don't already have a subscription, you can [sign up for a free 12 month Azure Subscription](https://azure.microsoft.com/en-us/free/) which includes up to $200 credit.
- [VS Code](https://code.visualstudio.com) or [Visual Studio 2017](https://visualstudio.microsoft.com/downloads/) (community is fine)
- [Bot Framework Emulator](https://github.com/Microsoft/BotFramework-Emulator/releases) (latest)
- [msbot command line tools](https://github.com/Microsoft/botbuilder-tools/tree/master/packages/MSBot#installation)
- [Github](https://github.com) or [Azure DevOps](https://devops.azure.com) repository 


### Step 1: Check out the sample bot

[Click here to see Eureka bot in action](https://eurekabot.azurewebsites.net/). Look for a chat icon in the bottom right corner and ask it a question based on this [FAQ](https://www.colorado.gov/pacific/dmv/faq-driver-license).


### Step 2: Create bot resources in Azure Portal

[Follow these instructions to establish a working bot](https://github.com/rob-derosa/EurekaBotGuides/blob/master/guides/echo_bot_azure.md). This way, you'll know your bot services are deployed and operational so now we can focus on code.


### Step 3: Build bot and deploy with CI/CD

[Follow these instructions to get your local dev environment configured](https://github.com/rob-derosa/EurekaBotGuides/blob/master/guides/local_build_and_deploy.md). In this section, we'll set up local debugging and testing, then configure a continuous pipeline when new code is pushed.


### Step 4: Create a QnAMaker knowledge base from an existing FAQ

[Follow these instructions to add a QnA Maker knowledge base](https://github.com/rob-derosa/EurekaBotGuides/blob/master/guides/qna_maker_portal.md). Add some question and answer intelligence into your bot by following these simple steps (your IT/HR/Support/etc teams will buy you lunch :)


### Step 5: Integrate QnA Maker into your bot code

[Follow these instructions to integrate a QnA Maker knowledge base into a bot](https://github.com/rob-derosa/EurekaBotGuides/blob/master/guides/integrate_qna_maker.md). Let's connect all the dots now that we have a knowledge base and a working bot.


### Step 6: Log conversation data to Cosmos using Middleware

[Add a rich media card welcome message and log conversations to external datastore](https://github.com/rob-derosa/EurekaBotGuides/blob/master/guides/conversation_logger.md). Let's greet the user with a card that includes video, text and buttons. We should also log the questions and answers along with the probability score from QnA Maker so we can ensure our users are getting accurate results - we'll dig into Cosmos for this.


### Additional Resources

 - [Bot Builder Samples](https://github.com/Microsoft/BotBuilder-Samples) - tons of samples for all kinds of things in both C# & node
 - [Adaptive Cards](http://adaptivecards.io) - build and preview cards on various channels with this awesome site
 - [QnA Maker](http://qnamaker.ai) - Build out your own knowledge bases using QnA Maker 
 - [LUIS](http://luis.ai) - Extend your bots funcionality by using natural language processing to fulfill custom actions from your users
 - [Bot Builder Tools](http://aka.ms/bbtools) - CLI tools for __QnA Maker__, __LUIS__ and __Dispatch__ (combine multiple QnA & LUIS models for a comprehensive bot experience) etc
 - [Cosmos DB](https://azure.microsoft.com/en-us/services/cosmos-db/) - Add multi-region, global replication and scale to your NoSQL databases with the click of a button 
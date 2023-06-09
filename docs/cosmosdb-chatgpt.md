# Instructions to run and play with the Azure Cosmos DB + OpenAI ChatGPT sample

## Prerequisites
- Contributor access to an Azure Subscription
- Reader access to the Azure OpenAI service provided for the Hackathon
- [VS Code](https://code.visualstudio.com/Download) installed
- [.NET SDK](https://dotnet.microsoft.com/en-us/download) installed
- [Git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git) installed 
- [GitHub account](https://github.com/join) (optional for option 2)

## Option 1: Quickstart to deploy
1. Open the URL in your browser: [`https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fvieiraae%2Fcosmosdb-chatgpt%2Fmain%2Fazuredeploy.json`](https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fvieiraae%2Fcosmosdb-chatgpt%2Fmain%2Fazuredeploy.json)
2. Ensure that the Azure subscription used for the Hackathon is selected. If you don't see the subscription, please reach out
3. Select or create a unique resource group used for you or your team
4. Set the Open Ai Resource Group and the Open Ai Resource Name with the values provided for the Hackathon. If you don't know those values, please reach out
5. Keep the other defaults and click `Review + create` and then hit `Create` to start the deployment
6. After the deployment finishes (should take around 3 minutes) go to your teams resource group and open the "App Service" resource.
7. Click on the "Default domain" property to open the app that was just deployed and start playing with it.

## Option 1: Quickstart to customize and run locally
1. Open a windows or linux terminal and execute the commmand: `git clone https://github.com/vieiraae/cosmosdb-chatgpt`
2. `cd cosmosdb-chatgpt`
3. `dotnet restore`
4. `code .` to open VS Code and start hacking. This sample uses [Blazor](https://dotnet.microsoft.com/en-us/apps/aspnet/web-apps/blazor) 
5. Open the `appsettings.json` file and set the Endpoint and Key values for the CosmosDb and OpenAI service.
6. `dotnet run`


## Option 2: Instructions to deploy the sample with your own repo
1. Fork your own copy of the https://github.com/vieiraae/cosmosdb-chatgpt repo (copy the main branch only)
2. Replace the `<your account or org name>` in the following url and open the URL in your browser: `https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2F<your account or org name>%2Fcosmosdb-chatgpt%2Fmain%2Fazuredeploy.json`
3. Ensure that the Azure subscription used for the Hackathon is selected. If you don't see the subscription, please reach out
4. Select or create a unique resource group used for you or your team
5. Set the Open Ai Resource Group and the Open Ai Resource Name with the values provided for the Hackathon. If you don't know those values, please reach out
6. Change the App Git Repository to point to YOUR repo - the App service is configure to deploy automatically files from the repo
7. Keep the other defaults and click `Review + create` and then hit `Create` to start the deployment
8. After the deployment finishes (should take around 3 minutes) go to your teams resource group and open the "App Service" resource.
9. Click on the "Default domain" property to open the app that was just deployed and start playing with it.

## Option 2: Instructions to customize and hack the sample with your own repo
1. Open a windows or linux terminal and execute the commmand: `git clone https://github.com/<your account or org name>/cosmosdb-chatgpt`
2. `cd cosmosdb-chatgpt`
3. `dotnet restore`
4. `code .` to open VS Code and start hacking. This sample uses [Blazor](https://dotnet.microsoft.com/en-us/apps/aspnet/web-apps/blazor) 
6. Commit and push to `main` branch
7. Go to the App service deployment center and hit `Sync` to deploy your changes. The web app will be publicly accessible so be mindful about any securiy concerns.
8. (Optional) If you want your changes to be deployed automatically with a CI/CD workflow on GitHub Actions, go to the App service deployment center, disconnect the existing source and configure a new one using GitHub and pointing to your repo.

## Notes
If you don't want to code in .NET and want to code in other language, you can leverage the following quick starts:
- [Quickstart: Deploy an ASP.NET web app](https://learn.microsoft.com/en-us/azure/app-service/quickstart-dotnetcore?pivots=development-environment-vscode&tabs=net70)
- [Create a Node.js web app in Azure](https://learn.microsoft.com/en-us/azure/app-service/quickstart-nodejs?pivots=development-environment-vscode&tabs=linux)
- [Create a PHP web app in Azure App Service](https://learn.microsoft.com/en-us/azure/app-service/quickstart-php?pivots=platform-linux&tabs=cli)
- [Quickstart: Create a Java app on Azure App Service](https://learn.microsoft.com/en-us/azure/app-service/quickstart-java?pivots=platform-linux-development-environment-maven&tabs=javase)
- [Quickstart: Deploy a Python (Django or Flask) web app to Azure App Service](https://learn.microsoft.com/en-us/azure/app-service/quickstart-python?tabs=flask%2Cwindows%2Cazure-cli%2Cvscode-deploy%2Cdeploy-instructions-azportal%2Cterminal-bash%2Cdeploy-instructions-zip-azcli)

Use the [Azure OpenAI Studio](https://oai.azure.com/) to access the [playground](https://learn.microsoft.com/en-us/azure/cognitive-services/openai/chatgpt-quickstart?pivots=programming-language-studio&tabs=command-line) to test the model and generate code for your use cases. Leverage the following guides for quick starts:
- [C#](https://learn.microsoft.com/en-us/azure/cognitive-services/openai/chatgpt-quickstart?pivots=programming-language-csharp&tabs=command-line)
- [Python](https://learn.microsoft.com/en-us/azure/cognitive-services/openai/chatgpt-quickstart?pivots=programming-language-python&tabs=command-line)
- [Python samples](https://github.com/Azure-Samples/openai)
- [REST](https://learn.microsoft.com/en-us/azure/cognitive-services/openai/chatgpt-quickstart?pivots=rest-api&tabs=command-line)

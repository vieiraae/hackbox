# Instructions to run the OpenAI Embeddings QnA Solution Accelerator

## Prerequisites
- Contributor access to the Azure resource group provided for the Hackathon
- Reader access to the Azure OpenAI service provided for the Hackathon

## Instructions to deploy the accelerator
- From the solution accelerator main github page navigate to the "Deploy on Azure (WebApp + Redis Stack + Batch Processing)" section.
- Click on the "Deploy to Azure" banner. This will open the Azure portal where you can configure the template for deployment.
- Use the following configurations in the parameter selection:
  - "Resource Group" field, select the Resource Group assigned to your workspace.
  - "Region" field, select "West Europe".
  - "Resource Prefix" field will be used to name the resources. Use any 2-13 string (without special characters).
  - "Open AI Name" field, use the name of the resource provided to you. Eg, If assigned the endpoint https://bh-openai-1.openai.azure.com/, use "bh-openai-1".
  - "Open AI Key" field, use the key provided to you.
  - If no translation and/or Form Recognizer is used, you can use "NA" for the following fields: "Form Recognizer Endpoint", "Form Recognizer Key", "Translate Endpoint", "Translate Key", "Translate Region"
 - Click "Review and Create".
 - Your deployment will be validated. If it succeeds, click "Create". If not, reach out to one of the mentors for help.
 - Once your deployment completes (should take a couple of minutes), navigate to your resource group in the Azure portal and identify the resource with suffix "-site".
 - The URL for your application will be present in the essentials pane, in the "Default domain" field. 
 - The first time you open the URL you can expect it to take a few seconds to load.

## Notes

Use the [Azure OpenAI Studio](https://oai.azure.com/) to access the [playground](https://learn.microsoft.com/en-us/azure/cognitive-services/openai/chatgpt-quickstart?pivots=programming-language-studio&tabs=command-line) to test the model and generate code for your use cases. Leverage the following guides for quick starts:
- [C#](https://learn.microsoft.com/en-us/azure/cognitive-services/openai/chatgpt-quickstart?pivots=programming-language-csharp&tabs=command-line)
- [Python](https://learn.microsoft.com/en-us/azure/cognitive-services/openai/chatgpt-quickstart?pivots=programming-language-python&tabs=command-line)
- [Python samples](https://github.com/Azure-Samples/openai)
- [REST](https://learn.microsoft.com/en-us/azure/cognitive-services/openai/chatgpt-quickstart?pivots=rest-api&tabs=command-line)

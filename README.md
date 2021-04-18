# flask-ml-azure-serverless
Deploy a Flask Machine Learning Application on Azure App Service

1. Clone the repo
2. Setup Virtual Environment
   1. ``` python3 -m venv ~/.flask-ml-azure ```
   2. ```source ~/.flask-ml-azure/bin/activate ```
3. Install dependencies by running:
   1. ``` make install ```
4. Create an Azure App Service and initially deploy the app by running:
   1. ```az webapp up -n <your-appservice>```
5. Verify the deploymet was successful by navigating to :  ```https://<your-appservice>.azurewebsites.net``` 
6. Change the line in make_predict_azure_app.sh to match the deployed prediction: ```-X POST https://<yourappname>.azurewebsites.net:$PORT/predict``` 
7. Create an Azure Devops Project [official documentaion](https://docs.microsoft.com/en-us/azure/devops/pipelines/ecosystems/python-webapp?view=azure-devops)
8. . Ensure you set up a new service connection via Azure Resource Manager and Pipeline
9. Create Pipeline

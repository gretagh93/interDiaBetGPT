# Hackaton - ON: The Beach 

## interDiaBetGPT

The idea of this project is to develop a Telegram interface utilizing ChatGPT, capable of answering complex questions about statistical data related to diabetes.

To achieve this, we use Iris IntegratedML and the large language model ChatGPT.

With Iris IntegratedML, we trained a machine learning (ML) model.

During the model validation process, we observed that the variance, R2, and other metrics were not satisfactory. As a result, we created additional models by varying the number of columns used and reducing the diabetes values to binary (0 represents patients without diabetes, and 1 represents patients with diabetes). Eventually, we obtained the 'DiabetesModelValidate31' model, which exhibited the best probability metric statistics. Additionally, we created a persistent field in the 'ValidateDataDiabetes' table that contains the prediction results for each row. This table serves as the basis for performing SQL queries to answer user questions."

To build the Docker image:
docker build -t hackathon-app . 

To run the container:
docker run -it --rm --name hackathon-app hackathon-app

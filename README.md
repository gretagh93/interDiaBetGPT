# interDiaBetGPT

Project inicialized in J ON: The Beach Hackaton with Intersystems.

The idea of this project is to develop a Telegram bot utilizing ChatGPT, which is capable of answering complex questions about statistical data related to healthcare.

We integrated Iris IntegratedML and Large Lenguage Model ChatGPT.

During the model validation process we have seen that the variance, R2, etc. metrics were not good. We have created other models by varying the number of columns used and reducing the diabetes values to (0 --> the patient does not have diabetes, 1--> the patient has diabetes). We finally got the 'DiabetesModelValidate31' model, which had the best probability metric statistics. Finally we have created a persistent field in the 'ValidateDataDiabetes' table that contains the result of the prediction for each row. This last table is the table on which we perform the SQL queries to answer the questions made by the user.

To build the Docker image:
docker build -t hackathon-app . 

To run the container:
docker run -it --rm --name hackathon-app hackathon-app

# Intro to Logistic Regression

## Definition
![Screenshot 2024-06-19 at 1 41 33 AM](https://github.com/imjustha/IBM_DataScienceProfessional_Certificate/assets/76855473/57c8783a-e12c-4893-9b28-13616c23c771)

## Logistic regression applications
- Predicting the probability of a person having a heart attack
- Predicting the mortality in injured patients
- Predicting a customer's propensity to purchase a product or halt a subscription
- Predicting the probability of failure of a given process or product
- Predicting the likelihood of a homeowner defaulting on a mortgage

## When is logistic regression suitable?

![Screenshot 2024-06-19 at 1 44 20 AM](https://github.com/imjustha/IBM_DataScienceProfessional_Certificate/assets/76855473/aaefd266-58e8-4880-bd89-ae3bf4cad2cb)

## Building a model for customer churn

![Screenshot 2024-06-19 at 1 45 14 AM](https://github.com/imjustha/IBM_DataScienceProfessional_Certificate/assets/76855473/22ef721f-f1de-4a67-8f52-26f0fa1e5bda)

# Logistic regression vs Linear regression

## Predicting customer income

![Screenshot 2024-06-19 at 1 46 05 AM](https://github.com/imjustha/IBM_DataScienceProfessional_Certificate/assets/76855473/c62fc3fc-aebe-4ecf-ab1a-4c7745e332bb)
![Screenshot 2024-06-19 at 1 46 36 AM](https://github.com/imjustha/IBM_DataScienceProfessional_Certificate/assets/76855473/64507780-b2ed-4df0-a9f3-1b5877be9ef1)
![Screenshot 2024-06-19 at 1 47 20 AM](https://github.com/imjustha/IBM_DataScienceProfessional_Certificate/assets/76855473/dd323372-94cb-45aa-b16d-a474ea170008)
![Screenshot 2024-06-19 at 1 47 53 AM](https://github.com/imjustha/IBM_DataScienceProfessional_Certificate/assets/76855473/d53a6990-32de-4ede-997d-1347ba0ca2a2)

## The problem

![Screenshot 2024-06-19 at 1 48 30 AM](https://github.com/imjustha/IBM_DataScienceProfessional_Certificate/assets/76855473/024b7663-64fa-4ab5-9627-228d989b5164)

## Sigmoid function in logistic regression

![Screenshot 2024-06-19 at 1 48 54 AM](https://github.com/imjustha/IBM_DataScienceProfessional_Certificate/assets/76855473/1cbffc27-bf28-4aab-aee6-67a62f18fdfe)

## Clarification of the customer churn model
- What is the output of our model?
  - P(Y=1|X)
  - P(Y=0|X = 1 - P(y=1|X)
 
  - P(Churn=1|income, age) = 0.8
  - P(Churn=0|income, age) = 1 - 0.8 = 0.2
    
![Screenshot 2024-06-19 at 1 50 58 AM](https://github.com/imjustha/IBM_DataScienceProfessional_Certificate/assets/76855473/a641e1a0-aa9f-4bc7-8f4d-9cb7d8922982)

## The training process

![Screenshot 2024-06-19 at 1 51 31 AM](https://github.com/imjustha/IBM_DataScienceProfessional_Certificate/assets/76855473/72b86dc6-cfb4-474b-87f9-8b4505c573c6)

# Logistic Regression Training

## General cost function

![Screenshot 2024-06-19 at 9 48 09 AM](https://github.com/imjustha/IBM_DataScienceProfessional_Certificate/assets/76855473/b0eeae23-03bb-46c1-8fbc-a4ec05a35604)

## Plotting the cost function of the model

![Screenshot 2024-06-19 at 9 48 50 AM](https://github.com/imjustha/IBM_DataScienceProfessional_Certificate/assets/76855473/af92bc87-d979-4c78-b0b5-fbbc23ef21b7)

## Logistic regression cost function

![Screenshot 2024-06-19 at 9 49 30 AM](https://github.com/imjustha/IBM_DataScienceProfessional_Certificate/assets/76855473/ec5a14c3-dbec-4f32-92ae-eaf6291f40f9)

## Minimizing the cost function of the model

- How to find the best parameters for our model?
  - Minimize the cost function
- How to minimize the cost function?
  - Using Gradient Descent
- What is gradient descent?
  - A technique to use the derivative of a cost function to change the parameter values, in order to minimize the cost
 

## Using gradient descent to minimize the cost

![Screenshot 2024-06-19 at 9 52 48 AM](https://github.com/imjustha/IBM_DataScienceProfessional_Certificate/assets/76855473/d19923d4-8b6d-4e40-993f-a92211753e66)


![Screenshot 2024-06-19 at 9 53 21 AM](https://github.com/imjustha/IBM_DataScienceProfessional_Certificate/assets/76855473/57e5dc31-04bb-495c-9993-2d27d3b744fb)


# (Support Vector Machines)[]
# (Multiclass Prediction)[]

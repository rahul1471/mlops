# Automation of Machine Learning Model Training using Jenkins Pipeline(MlOps)

### Project Description:

1. Jenkins tool will fetch the machine learning program(task3.py) from github and copy to the specific folder of the admin workstation whenever the changes will occur to the code on repository.
2. Then, Jenkins will trigger the next job which will run that ML code(task3.py) on admin's workstation using docker image of specific configuration required for that code(in our case: CNN).
3. Then, after the execution of 2nd job, 3rd job will be trigger which will find the accuracy of the model.
4. Now, 4th job will be trigger and send the information about model to the specifies email address.
5. Now, 5th job will be trigger and check whether the trained model having required accuracy or not. If it does not then it will change the hyper-parameters of the ML code and again run it till the accuracy reach its specified mark and at last it will notify 'SUCCESS'.

## Screenshots of the project:

### Email configuration on Jenkins:
![Email Configuration](/Screenshots/email.jpg)

### Job1 configuration: where we will fetch the code from github and copy it to the admins specific directory.
![Job 1](/Screenshots/job1.jpg)

![Job 1](/Screenshots/job1_2.jpg)

![Job 1](/Screenshots/job1_3.jpg)

#### output of Job1:
![Job 1 output](/Screenshots/job1_output.jpg)


### Job2 configuration: where we will run the ml code to the specific docker environment.
![Job 2](/Screenshots/job2.jpg)

#### output of job2:
![Job 2](/Screenshots/job2_output1.jpg)

![Job 2](/Screenshots/job2_output2.jpg)

### Job3 Configuration: It will find the accuracy of the model and if model is not trained then again it will try to train it on different custom docker environment.

![Job 3](/Screenshots/job3.jpg)

#### Job3 output:

![Job 3 output](/Screenshots/job3_output1.jpg)

### Job4 Configuration: It will send the results of the trained model to the specified email address.

![Job 4](/Screenshots/job4_1.jpg)

![Job 4 email configuration](/Screenshots/job4_email.jpg)

#### Job4 output:

![Job 4 output](/Screenshots/job4_output.jpg)

### Job5 Configuration: It will check the accurcy and if it does not meet the requirment, it will change the hyper-parameter of ML code and again train the model till the accuracy will rerach the required accuracy.

![Job 5](/Screenshots/job5_1.jpg)

![Job 5](/Screenshots/job5_2.jpg)

#### Job5 output:

![Job 5 output](/Screenshots/job5_output.jpg)

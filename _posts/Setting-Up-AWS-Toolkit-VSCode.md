# Setting up AWS Toolkit at VSCode

# Prerequisites
- An active AWS account can be signed up [here.](https://portal.aws.amazon.com/billing/signup#/start/email/)

- Install VSCode [here.](https://code.visualstudio.com/)

- Install AWS Toolkit Extension [here.](https://marketplace.visualstudio.com/items?itemName=AmazonWebServices.aws-toolkit-vscode)  


# Getting credentials from an AWS account

## Login and navigate to IAM

- Login to the account [here](https://aws.amazon.com/console/)
- Navigate to [IAM.](https://us-east-1.console.aws.amazon.com/iamv2/home)

  ![IAM Management Console](./Setting-Up-AWS-Toolkit-VSCode/2022-10-08%2019_16_15-IAM%20Management%20Console.png)

- **Before creating a new programmatic user we need to create a new user group as we need that while creating a user.**


## Create User Group
- Click on User groups

  ![User groups](./Setting-Up-AWS-Toolkit-VSCode/2022-10-08%2019_54_13-IAM%20Management%20Console.png)

- Click on Create group
  ![Create group](./Setting-Up-AWS-Toolkit-VSCode/2022-10-08%2020_06_48-IAM%20Management%20Console.png)

- Fill in basic details
  ![alt](./Setting-Up-AWS-Toolkit-VSCode/2022-10-08%2021_09_51-IAM%20Management%20Console.png)

  Select policies to attach as shown below
  ![alt](./Setting-Up-AWS-Toolkit-VSCode/2022-10-08%2021_17_43-IAM%20Management%20Console.png)

  Once a User Group is created it looks as follows!
  ![created](./Setting-Up-AWS-Toolkit-VSCode/2022-10-08%2021_22_48-IAM%20Management%20Console.png)


## Create A Programatic User
- Click on Users
  ![Add User](./Setting-Up-AWS-Toolkit-VSCode/2022-10-08%2019_25_58-IAM%20Management%20Console.png)

- Fill in basic details as following
  ![Basic details](./Setting-Up-AWS-Toolkit-VSCode/2022-10-08%2019_30_28-IAM%20Management%20Console.png)

- Set Permission via user group
  
  User Group let you specify permission for multiple users more details can be found [here](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_groups.html)

  In a previous step we have already created a user group `Group_Developer` will use that to assign policies to the user.

  ![setting user permission](./Setting-Up-AWS-Toolkit-VSCode/2022-10-08%2021_34_58-IAM%20Management%20Console.png)

- Skip tags for now
![tag](./Setting-Up-AWS-Toolkit-VSCode/2022-10-08%2021_40_57-IAM%20Management%20Console.png)

- Review your inputs
![User Review](./Setting-Up-AWS-Toolkit-VSCode/2022-10-08%2021_45_43-IAM%20Management%20Console.png)

## Download user credentials CSV
- Download User Credentials
![CSV Download](./Setting-Up-AWS-Toolkit-VSCode/2022-10-08%2021_47_04-IAM%20Management%20Console.png)

- Get credentials

# Install AWS Tool Kit Extension

 Install THE extension mentioned below

 ![alt](./Setting-Up-AWS-Toolkit-VSCode/2022-10-08%2021_52_31-Extension_%20AWS%20Toolkit%20-%20Visual%20Studio%20Code.png)
  
once installed it may ask for admin right just say yes.

# Setting up Client Credentials

- Open VS Code

- Open Command Pallete via `Ctrl + Shift + P`

![alt](./Setting-Up-AWS-Toolkit-VSCode/2022-10-09%2000_00_32-Get%20Started%20-%20Visual%20Studio%20Code.png)

### Create Credentials profile

- Add Name to profile
![image](./Setting-Up-AWS-Toolkit-VSCode/2022-10-09%2000_04_53-Get%20Started%20-%20Visual%20Studio%20Code.png)

- Enter AWS Access Key that you downloaded from AWS
![AWS Access Key](./Setting-Up-AWS-Toolkit-VSCode/2022-10-09%2000_07_40-Get%20Started%20-%20Visual%20Studio%20Code.png)

- Enter Aws Secret Key from `user credentials.csv`
![alt](./Setting-Up-AWS-Toolkit-VSCode/2022-10-09%2000_10_14-Get%20Started%20-%20Visual%20Studio%20Code.png)

- After pressing enter, your credentials will be saved to aws config

![alt](./Setting-Up-AWS-Toolkit-VSCode/2022-10-09%2000_12_46-credentials%20-%20Visual%20Studio%20Code.png)

- After saying yes, AWS explorer will list down all the resources associated with the account.

For eg:
![alt](./Setting-Up-AWS-Toolkit-VSCode/2022-10-09%2000_18_00-credentials%20-%20Visual%20Studio%20Code.png)

> **Note**: I have created an s3 bucket on aws account named `myweather-api-bucket`
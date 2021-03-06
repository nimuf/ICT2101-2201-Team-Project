# ICT2101-2201-Team-Project
![image](https://user-images.githubusercontent.com/75081645/144783400-5a3f18c7-ddc0-4288-b13c-a080456b5e9e.png)

## Team Members
- Ong Sheng Wei Kenrick (2000909)
- Png Han Zheng (2000970)
- Chong Fu Min (2002039)
- Fashshila Yasmin D/o Mohammed Yunoos (2001301)
- Lee Yen Ning (2001775)

## Getting Started (for windows)
- Make sure you have at least Python 3.8.5 and Visual Studio Code

## Setup
**Clone the Project Repo**
1. Open a shell and navigate to desired directory to save the project folder
2. Execute the git clone command
git clone https://github.com/nimuf/ICT2101-2201-Team-Project.git

**Setting up the Project Environment**
1. Create and activate a virtual environment named .venv
(py -3 -m venv .venv
.venv\scripts\activate)

2. Open the Command Palette and select interprete in your project folder that starts with ./.venv or .\.venv

![image](https://user-images.githubusercontent.com/75081645/144780760-3214cab5-2f79-40de-b4bd-f6d8873bc169.png)

3. Execute the command python -m pip install --upgrade pip and python -m pip install flask

![image](https://user-images.githubusercontent.com/75081645/144780692-4dcfa933-8fa6-45a1-b023-95a62b4aa05d.png)

**How to run**
1. Navigate to the root directory of the project (where app.py is)
2. Start the debugger by selecting the Run > Start Debugging 
3. Open Google chrome and navigate to http://127.0.0.1:5000/
# Prototype Implementation
## Work Management
**Individual Branch Management**
1. Each team member should perform their own changes in their own individual branch
2. Pushing to each individual branch should only be done when the component done is in a **working** version

**Main Branch Management**
1. Only completed individual branches can be merged into the main branch
2. Pull requests to merge the individual branch should be done through Github's web ui

**Branch Management Diagram**

![image](https://user-images.githubusercontent.com/72655216/144869560-d46157c0-bc88-4971-97fc-06a6d0949d7a.png)

**Git WorkFlow Diagram**

![image](https://user-images.githubusercontent.com/72655216/144869616-c8ad0fdd-2072-4dd6-9ff9-52690e5a1325.png)

## Black Box Testing
**System State Diagram**

![image](https://user-images.githubusercontent.com/72655216/144748676-738bda0d-add5-429d-89e0-3d1f4eb73c37.png)

**System Test Cases**

![test case ss1](https://user-images.githubusercontent.com/73540954/144647626-88e5e8a5-705b-48cc-b492-e6ee54313cdb.JPG)
![test case ss2](https://user-images.githubusercontent.com/73540954/144647630-4a2c0978-8941-45fe-b4a0-4e3cb9a4263d.JPG)
**System Test Video**

Click Here:
[![IMAGE ALT TEXT HERE](https://img.youtube.com/vi/Xvw59fAYJm0/0.jpg)](https://www.youtube.com/watch?v=Xvw59fAYJm0)

# White Box Testing
**Selected Class for White Box Testing**

![image](https://user-images.githubusercontent.com/72655216/144747751-6a190a92-22ec-4336-9b6b-9846bd84dc1e.png)
![image](https://user-images.githubusercontent.com/72655216/144747835-bebc8071-c760-4d14-acfd-c1b33ecd02a3.png)


**Car controller class**

We have chosen car controller class as we feel that it is the most important and interesting class. The backend logic of the connection from the robotic car and the website is located inside this car controller class. 

Functions:
1. Connect Car
    - Checks the status of the car. If the car is currently disconnected, change the status of the car to connected.
    
2. Disconnect Car
    - Checks the status of the car. If the car is currently connected, change the status of the car to disconnected.
    
3. Send Data
    - Used for sending the difficulty level of the programming tasks in order for the car to read its movement instructions from.
    
4. Receive Data
    - Used by our website to display the data of the car onto our dashboard.
    
5. Detect Obstacle
    - Checks the sensor status of the car. If there is an obstacle detected, return True. Else, return False.


**Test Cases**

![image](https://user-images.githubusercontent.com/72655216/144748039-bc88b6a9-03cb-4c52-af63-754445a13545.png)
![image](https://user-images.githubusercontent.com/72655216/144748050-082c3a2c-5c20-445b-a626-259a866b4772.png)
![image](https://user-images.githubusercontent.com/72655216/144748057-9ec86246-cca6-44cb-995d-c17588d5adb9.png)

**How to run the test cases:**

First, we need to install the Code Coverage library. Run the following command inside your command prompt:

- $ pip install coverage

Once the Code Coverage library is installed, change directory to your folder location by using the "cd" command:

- $ cd (folder location)

Afterwards, run the following code to run the Code Coverage on the car.py file:

- $ coverage run car.py

Then, run the following code to view the report (result) of the Code Coverage:
    
- $ coverage report


We have implemented 3 different test cases for statement coverage testing. The 3 test cases are as follow:
1. Test case 1
   
   Car status:
    - Car is not connected.
    - There are no obstacles detected.
    
   Functions called:
    - Connect Car in order to connect the current disconnected car.
    - Send Data in order to send current difficulty level programming tasks for the car to read.
    - Detect Obstacle to check the sensor status.

2. Test case 2
   
   Car status:
    - Car is connected.
    - There are obstacles detected.
   
   Functions called:
    - Disconnect Car in order to disconnect the current connected car.
    - Send Data in order to send current difficulty level programming tasks for the car to read.
    - Receive Data in order to display the data of car onto our dashboard.
    - Detect Obstacle to check the sensor status.

3. Test case 3
   
   Car status:
    - Car is connected.
    - There are no obstacles detected.
   
   Functions called:
    - Get Speed located inside the entity Car class to get the current speed of the car.
    - Set Speed located inside the entity Car class to set the speed of the car.


**Coverage results:**

Test case 1:

![image](https://user-images.githubusercontent.com/72655216/144748437-10f184ef-08ab-4fca-b44c-bd0f9dfa1aba.png)


Test case 2:

![image](https://user-images.githubusercontent.com/72655216/144748459-3cfe8e9a-0130-477c-aebd-c47a61e508a0.png)


Test case 3:

![image](https://user-images.githubusercontent.com/72655216/144748494-ec710805-c57f-4f42-bbcf-d73d7f580a11.png)


Total coverage of all 3 test cases:

![image](https://user-images.githubusercontent.com/72655216/144748522-801fb384-4f86-4c1f-ab36-4a8308055b66.png)
![image](https://user-images.githubusercontent.com/72655216/144748537-7b333c7f-0f7e-4208-bf69-0e1658122359.png)


**White Box Testing Video**

Click here:
[![IMAGE ALT TEXT HERE](https://img.youtube.com/vi/cA57TA9uwhE/0.jpg)](https://www.youtube.com/watch?v=cA57TA9uwhE)



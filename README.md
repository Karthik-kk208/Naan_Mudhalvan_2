# Naan_Mudhalvan_2
Naan_mudhalvan_final_project 
OPTIMIZING USER, GROUP, AND ROLE MANAGEMENT THROUGH ACCESS CONTROL AND WORKFLOWS  USING SERVICENOW

Problem Context:
                       In a small project environment, a Project Manager (Alice) and a Team Member (Bob) are responsible for delivering tasks. However, the absence of well-defined roles, access restrictions, and structured workflows often creates confusion in responsibilities, accountability, and progress monitoring.
 **Objective:** To implement a robust system for user, group, and role management within ServiceNow, ensuring clear access controls and streamlined workflows for efficient project delivery. **Solution Overview:** This project aims to leverage ServiceNow's capabilities to establish a comprehensive framework for managing users, groups, and roles. 

 Objectives:
1. Role Definition: Clearly outline the duties of Alice as Project Manager and Bob as Team Member, ensuring both responsibility and access boundaries are transparent.
2. Access Control: Introduce mechanisms that limit Bob’s ability to create or edit projects beyond his assigned tasks, while still allowing him to view and update his responsibilities.
3. Workflow Organization: Establish a structured process that enables Alice to assign work, track task progress, and oversee completion in a timely and efficient manner.

Key Skills/Tools: Users, Groups, Roles, Tables, Access Control Lists (ACL), Workflow/Flow Designer.

STEPS :

Activity 1: Create Users
1. Open service now
2. Click on All >> search for users
3. Select Users under system security
4. Click on new
5. Fill the following details to create a new user
6.Click on submit
Create one more user:
7. Create another user with the following details
8. Click on submit

Activity 2: Create Groups
1. Open service now.
2. Click on All >> search for groups
3. Select groups under system security
4. Click on new
5. Fill the following details to create a new group
6. Click on submit.

Activity 3: Create roles
1. Open service now.
2. Click on All >> search for roles
3. Select roles under system security
4. Click on new
5. Fill the following details to create a new role
6. Click on submit.
Create one more role:
 7.Create another role with the following details 
8.Click on submit

Activity 4: Create Table
 1. Open service now. 
2. Click on All >> search for tables
 3. Select tables under system definition
 4. Click on new 
5. Fill the following details to create a new table 
Label: project table 
Check the boxes Create module & Create mobile module 
6. Under new menu name: project table 
7. Under table columns give the columns 
8. Click on submit

Activity 5: Assign users to project team group
 1.Open service now.
 2.Click on All >> search for groups 
3.Select tables under system definition 
4.Select the project team group 
5.Under group members 
6.Click on edit
7.Select alice p and bob p and save

Activity 6: Assign roles to alice user 
1.Open servicenow.Click on All >> search for user 
2.Select tables under system definition
3.Select the project manager user
4.Under project manager 
5.Click on edit
 6.Select project member and save 
7.click on edit add u_project_table role and u_task_table role 
8.click on save and update the form. 

Activity 6.a: Assign roles to bob user 
1. Open servicenow.Click on All >> search for user 
2.Select tables under system definition 
3.Select the bob p user 
4.Under team member 
5.Click on edit 
6.Select team member and give table role and save 
7. Click on profile icon Impersonate user to bob 
8. We can see the task table2. 

Activity 7: Assign table access to application 
1. while creating a table it automatically create application and module for that table 
2. Go to application navigator search for search project table application 
3. Click on edit module 
4. Give project member roles to that application 
5. Search for task table2 and click on edit application. 
6. Give the project member and team member role for task table 2 application

Activity 8: Create ACL 
1. Open service now. 
2. Click on All >> search for ACL 
3. Select Access Control (ACL) under system security 
4. Click on elevate role 
5. Click on new 
6. Fill the following details to create a new ACL 
7. Scroll down under requires role 
8. Double click on insert a new row 
9. Give task table and team member role 
10. Click on submit 
11. Similarly create 4 acl for the following fields 
12.Click on profile on top right side 
13.Click on impersonate user 
14.Select bob user 
15.Go to all and select task table2 in the application menu bar 
16. Comment and status fields have the edit access 

Activity 9: Create a Flow to Assign operations ticket to group  
1. Open service now. 
2. Click on All >> search for Flow Designer 
3. Click on Flow Designer under Process Automation.
 4. After opening Flow Designer Click on new and select Flow. 
5. Under Flow properties Give Flow Name as “task table”. 
6. Application should be Global. 
7. Click build flow. 
next step: 
1. Click on Add a trigger 
2. Select the trigger in that Search for “create record” and select that. 
3. Give the table name as “task table”. 
4. Give the Condition as Field: ‘status’ Operator: ‘is’ Value: ‘in progress’ 
                                        Field: ‘comments’ Operator: ‘is’ Value: ‘feedback’
                                        Field: ‘assigned to’ Operator: ‘is’ Value: ‘bob’ 
5. After that click on Done.
 Next step: 
1. Click on Add an action. 
2. Select action in that, search for “update records”. 
3. In Record field drag the fields from the data navigation from Right Side (Data pill) 
4. Table will be auto assigned after that 
5. Add fields as “status” and value as “completed” 
6. Click on Done. 

Next step: 
1. Now under Actions. 
2. Click on Add an action. 
3. Select action in that, search for “ask for approval”. 
4. In Record field drag the fields from the data navigation from Right side 
5. Table will be auto assigned after that 
6. Give the approve field as “status”
 7. Give approver as alice p 
8. Click on Done. 
9.Go to application navigator search for task table. 
10. It status field is updated to completed 
11.Go to application navigator and search for my approval 
12.Click on my approval under the service desk. 
13. Alice p got approval request then right click on requested then select approved 

Conclusion:
                      This approach provides a streamlined system for managing projects by defining roles, applying access restrictions, and organizing workflows. It helps the team collaborate effectively, improves accountability, simplifies task tracking, and ensures successful project delivery.


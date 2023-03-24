## DataModelling-SF-Admin
#### DataBase and Object
#### DataBase
- we generally need to store data in Excel Sheet
- So,Fetching the data from Excel Sheet having thousands of records are diffiuclt
- Identifying the records uniquely is difficult
- so,for all of these things we came up with a solution called database
- In which fetching the records,Updating the records, stroing the records and managing the data becomes easier
- But In Excel Sheet it is not as much as easy
- So, from file System we need to move for database because we want organised collection of data to be stored and maganed very easily
- So,In Normal database like Mysql or SQL or ORACLE the data get stored in database obviously But in the database we need to have a table which stores the information in a 
   structured format and generally a table includes two things column and rows
- Columns are basically the attributes like what kind of data we can store for every student
- Rows are basically instances of that table which stores the information  of students in that particular table  listout the actual information
- Salesforce database is the similar way as Relational database for all of us.Like down there is something different that you can't realize later
- Salesforce also stores the infromation in tabular format or in a table only but the terminology is different when its came to salesforce
- When its comes to SalesForce the terminology that we use for the table is Object
- So,whenever we want to create about a particular table we will say an Object
- An Object will represent an entity which stores the particular information or particular type of information in our database
- So,If you want to create an information for student we can create the student Object
- If you want to store an info of client we are going to use client Object
- So,in Salesforce we used to call columns as fields
- Rows are used to call as records
#### Different types of Object
There are two different types of Objects
1.Standard Object
2.Custom Object

###### Standard Object ::
- Standard Object is which already present in the salesforce and given by salesforce as a part of its products
- Eg: Contacts, Leads, Accounts

##### Custom Object : :
- The Objects which we create accordingly to our needs and requirements are called as custom Objects
- Whenever think about standard Objecr you align your mind that it is a prebuild thing
- We can Customize the standard Object or standard things is but we cannot delete it/remove it completely
- But when comes to custom object we can remove or delete or customize the way we want

# Apps :

- In salesforce an App is nothing but three things-Name,Logo and Tabs(Set of tabs)
- what that means is whenever you create an app
- There are two different types of apps
- i) Standard apps ==> Sales App
- ii) Custom Apps ==> which we are going to create

## Tabs
- Tab is basically an UI component which allows to acess you to particular functionality
- So when we talk about an application having differnet tabs means an application having differnent functionality
- An application can have different functionality with different tabs
- A single tab has its own functionality
- There are different types of tabs as well
- standard object tabs,custom object tabs,visualforce tab,lightning tab,web tab

- when the  custom app is deleted it doesn't effect any tab or object created in it
- when the custom tab deleted the objects associated with it will not gets deleted
- whenever we delete the custom object the tab associated to it will gets deleted and the tab will be automatically removed from the tab as well

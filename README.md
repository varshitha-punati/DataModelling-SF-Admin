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
 setup=>object manager =>create custom object=>select optional features(allow reports,Allow activities ,Tarck Field History,Allow in Chatter groups)
# Apps :

- In salesforce an App is nothing but three things-Name,Logo and Tabs(Set of tabs)
- what that means is whenever you create an app
- There are two different types of apps
- i) Standard apps ==> Sales App
- ii) Custom Apps ==> which we are going to create
-- setup=> App Manager => New Lightning App
## Tabs
- Tab is basically an UI component which allows to acess you to particular functionality
- So when we talk about an application having differnet tabs means an application having different functionality
- An application can have different functionality with different tabs
- A single tab has its own functionality
- There are different types of tabs as well
- standard object tabs,custom object tabs,visualforce tab,lightning tab,web tab
#### Important points
- when the  custom app is deleted it doesn't effect any tab or object created in it
- when the custom tab deleted the objects associated with it will not gets deleted
- whenever we delete the custom object the tab associated to it will gets deleted and the tab will be automatically removed from the tab as well

-----------------------------------------------------------------------------------------------------------------------------
### Fields

- Fields are used to store the different attributes of the same record/ same entity or same Object
- There are two different types of fields
- 1) Standard field --> The fields created by salesforce on its own
- 2) Custom field --->The fields which created by us for requirement

-standard fields we cannot delete and custom fields we can delete
- Login=>salesforce=>Setup=>object
- if you observe in every custom object there are some fileds are there like owner,created by,last modified by(which we created while creating object)
- if you got objects if there is no delete option then it is standard object otherwise it is custom object
- Goto =>setup=>Object Manger=>student Object=>Fields and Relationships=>New
- #### Datatypes of fields
- 1.checkbox-->used to select true or false(we need check or uncheck based on the requirement)
- 2.currency-->it is used to enter the currency in INR or Dollars or other currency
- 3.Date ----> It Allows user to enter a date or pick a date from pop up calender
- 4.Date / Time ---> It allows users to enter a date and time or pick a date from a pop up calender
- 
- <img width="566" alt="image" src="https://user-images.githubusercontent.com/72751737/227424306-2815d60a-a38a-4dd9-94d4-b9ea92a48a5a.png">
- 5.Email ----->Allows users to enter an email address,which is validated to ensure proper format
- 6.Geolocation ---> Allows users to define Locations.Includes latitude and Longitude components and can be used to calculate distance(latitude and longitude)
- 7.Number--> Allows users to enter any number.Leading Zeros are removed
- 8. Percent-->Allows user to enter a percentage number,for example, '10' and automatically adds the percen sign ot the number
- 9.phone--->Allows user to enter any phone number.Automatically formats it as phone number
- 10.Picklist--Allows users to select a value from list you define
- 11.picklist(multi-select)-Allows users to send Multiple values from a list you define
- <img width="796" alt="image" src="https://user-images.githubusercontent.com/72751737/227424443-fec6710c-e96d-4247-ac2d-cfa1e32fea66.png">

## Global Picklist
- If the picklist that is common for most of the objects and we need to reuse in different object then we can create global picklist
- so,for that goto=>picklistvalueset=>create one picklist
- now goto =>object manager=>fields and relationships=>new=>piclist=>next=>select values
 ## Field Dependency
 - `Field dependency means, controlling a fields value based on the other field.
 -  For example, there are two fields called Country & State. 
 -  I want to display only states related specific selected country when I select country.
 #### Controlling field
 - The Field which controls the values of another fields
 #### Dependent Fields
 - The Fields whose values gets controlled by controlling Field
- Field Dependency works on three different datatypes
-  picklist, multiselect picklist and checkbox
- Data Type------->	Controlling field--------------->	Can we define as Dependent field
- Standard Picklist	 ------------------------>     Yes------>No
- Custom Picklist	  -------------------------->     Yes------>Yes
- Multi-Select pick list---------------------->  	 No------->Yes
- standard Checkbox--------------------------->	    Yes------->No
- custom checkbox----------------------------->     Yes-------->No
-
- In fields and relationships there is a field dependency
 - Go to  setup menu and select the object you want to create field dependency.
– Click on filed dependency button & select controlling and dependent fields. See the below screen for reference.
![image](https://user-images.githubusercontent.com/72751737/227427143-208ccd9e-58f1-48dd-b076-b0e37bc5a614.png)
- Click on continue and select dependent fields under controlling fields. click on include & then Save. see the below screen for reference.
- ![image](https://user-images.githubusercontent.com/72751737/227427222-80f65965-ecd8-441b-81c1-a7a09a1b515a.png)
- Here you can include values

### Validation Rules
- Validation rules in salesforce contains a formula or expressions that evaluates the data in one or more  fields in a record to meet the standards and returns a value “True” or “False”. Validation rules displays error message to the user when the Condition is “False”.
- Suppose in any website for phone number you tried enter the number which is not 10 digits then the phone nymber connect it will say
- so,these are particular checks placed on evrything like forms. So that the data gets entered in the database is validated and right
- Whenever you save a record it will goes to the validation rule on that object which you want to validate on which you want to be data to be stored
- whenever you save a record it will goes to the validation rule and it validates its formula and these formual can return true or false
- validation rules have two things
- 1.Formula
- 2.Error
- If it returns false value then the record gets saved 
- it if returns true then the error message will shown
- AND(
	Checkbox_Example__c = True,
	ISBLANK(TEXT(Industry))
)

### Roll-Up Summary field
- Roll-up summary fields work by calculating a summary value from child records and displaying it on a parent record. For example, a roll-up summary field on an account record could calculate the total value of all opportunities associated with that account
- In order to create a roll-up summary field, you must first create a relationship between the parent object and the child object. This relationship must be a         master-detail relationship, as roll-up summary fields cannot be created on lookup relationships.
- Once the relationship is established, you can create a roll-up summary field on the parent object. 
- You can choose from a variety of summary functions, such as sum, average, count, minimum, and maximum, and specify which field on the child object should be used in the calculation.
- The roll-up summary field is automatically updated whenever child records are created, updated, or deleted, ensuring that the summary value is always accurate and up-to-date.

 ##### CREATING ROLL-UP SUMMARY FIELDS
- Creating roll-up information summary fields in Salesforce is a straightforward process, but it does require some planning and setup.
- Here’s how to create a roll-up summary field:
- Establish a master-detail relationship between the parent object and the child object.
- Navigate to the parent object’s page layout and click on the gear icon in the upper right corner.
- Click on “Edit Object” and scroll down to the “Fields” section.
- Click on “New” and select “Roll-Up Summary” as the field type.
- Name the field and select the object that you want to roll up data from.
- Choose the summary function and field to roll up.
- Select any additional filter criteria or grouping options, if necessary.
- Save the field and add it to the page layout.

#### Schema Builder
- Schema builder salesforce is a pictorial representation of all objects, fields and their relationships in Salesforce.com.
- It provides a dynamic environment to view and modify all the objects and their relationships.
- How to access Schema builder salesforce?
- To build Salesforce Schema Builder go to Setup | Build | Schema Builder.
- Schema Builder displays all standard and custom objects in our organisation. We have many option to view object like All Objects, Selected Objects, Standard          Objects, Custom Objects, System Objects. Depending upon our requirement we can select the objects that to be displayed. When we select custom objects it displays     all object in pictorial representation as shown below.
![image](https://user-images.githubusercontent.com/72751737/227431371-49c820ba-74cd-4bd8-974e-c28775e48fd0.png)

## Relationships
- Relationship is the way in which two or more people or things connected with each other. 
- The way they connected will be of different types like wise in salesforce 
- There are 4 different types of relationships in salesforce.
- Master-Detail relationship.
- Lookup Relationship.
- Many-Many Relationship.
- Hierarchy Relationship (we can not use this relationship).
- # 1. Master-Detail relationship:

- In this type of relationship, one object acts as a master and other act as a detail object. In other words, this relationship acts as a parent-child relationship. - We use this type of relationship when we want to bound two objects tightly or closely dependent on each other.
- The behavior of Master-Detail relationship:
- When a master record gets deleted, its related child/detail record automatically gets deleted.
- In a master-detail relationship both the objects are strongly coupled to each other.
- Sharing and security settings of the detail records are inherited as per their master settings.
- We can define this relationship in between custom objects and in between standard and custom objects. Note that, the standard object must be on the master side 	while creating relationships between standard and custom objects. 
- We can also have roll-up summary fields in master-detail relationships which helps us to calculate values from child records by using aggregate functions like  	Count, Sum,  Min, Max.
- The master-detail field is required on the detail record’s page layout.
- We can only create a maximum of 2 master-detail relationships per object. In a master-detail relationship both the objects are strongly coupled to each other.

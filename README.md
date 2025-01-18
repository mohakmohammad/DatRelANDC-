Main Functions Explanation

PrintAllContacts
This function displays all contacts whose first name starts with a specific letter.

SqlDataReader is used to read data from the database.

Parameters are used to avoid SQL Injection vulnerabilities.

Called in Main:

csharp
Copy
Edit
PrintAllContacts("j");

GetFirstName
This function returns the first name of a contact based on its id.

Uses ExecuteScalar to fetch the single value (first name).

Called in Main:

csharp
Copy
Edit
Console.WriteLine(GetFirstName(5));

FindContactId
Finds a contact based on its id and returns its information via stContact structure reference.

Returns true if the contact is found and false if it is not found.
Call in Main:

csharp
Copy
Edit
if(FindContactId(125, ref ContactInfo))
AddNewContact
Adds a new contact to the database and returns the ID of the contact who was inserted.

Uses SCOPE_IDENTITY() to retrieve the new ID.

Call in Main:

csharp
Copy
Edit
AddNewContact(Contact);
UpdateContact
Updates a contact's information based on its ID.

Uses ExecuteNonQuery to find out how many rows were affected.
Call in Main:

csharp
Copy
Edit
AddNewContact(11, ContactInfo);
DeleteContact
Deletes a contact based on its ID.

Checks whether the deletion was successful based on how many rows were affected.
Call in Main:

csharp
Copy
Edit
DeleteContact(2);
Project Features
The application provides a foundation for programming database-related applications using C# and SQL Server.
Uses SQL queries with parameters to protect against SQL Injection vulnerabilities.
Relies on the stContact structure to store contact information in an organized manner.

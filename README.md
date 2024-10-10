# Books API testing from Postman 🧪

During my learning on January 2024 about REST-API I had burried repository. Finally I had some free time to describe it and marked as finished.
You can read more about this API here: https://www.postman.com/postman/postman-library-api-v2/documentation/udathed/postman-library-api-v2-docs this is official link.

For download .json file go to Postman Collections folder and download MyCollection.json
After completing it open Postman tool and Import MyCollection.json

This API is simple and easy to understand. This is how hierarchy is presented:

![Postman Flow](https://github.com/user-attachments/assets/7123848c-6630-4ec3-b810-683e7c2d0ed0)

On each endpoint I wrote some validations in JavaScript programming language. I initialized local and collection variables.  
Variable name BookId is dynamic. Every each request endpoint named "add book" will change BookId value.

For testing purpose you can change JSON body on endpoint /books
![Books](https://github.com/user-attachments/assets/2d94a368-3e39-4caf-8afe-4f9f2a6ce870)

When do you want update your data you can do it on this endpoint /books/:id
I choosed two lines: "checkedOut" and "yearPublished". Of course you can define different one or add more but remember you have to change scripts if no you will get errors.
![Update](https://github.com/user-attachments/assets/4df05d2a-0916-4474-9e7c-8795011776f5)







This is how script looks like on one endpoint:



![GetAllBooks](https://github.com/user-attachments/assets/8ab52a82-cb6d-4a64-9d18-e2b2f9ec3b8d)


You can run whole collection by runner on Postman. I recommend to run endpoints by following order:

![Runner](https://github.com/user-attachments/assets/abcec051-d929-49c2-b367-c8b5d8055b39)

You can run collection by Newman via PowerShell CLI. For that you need:

-Node.js  https://nodejs.org/en/download/package-manager. After instalation you can open cmd and write command node --version
-Install Newman from this command line: -npm install -g newman. After instalation you can write similar command line like below. Instead node use newman --version

Open PowerShell go to directory where you downloaded MyCollection.json and use CLI: newman run .\MyCollection.json

![Newman](https://github.com/user-attachments/assets/81895699-9e97-4f98-9e3a-b1f30ca12b08)

For add an additional report install third-party addon: npm install -g newman-reporter-htmlextra

https://www.npmjs.com/package/newman-reporter-htmlextra

When command will finish you will get html report looks like this:
I attached file in to this repository like named: Postman_Books_Library + time_stamp. You can download it easily.
![Report](https://github.com/user-attachments/assets/0799bef2-e47d-44d3-8395-c62578d2eadb)





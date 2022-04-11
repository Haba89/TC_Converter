# TC_Converter - Solution for automating payments from travel agencies

Intro:

Due to a lot of manual handling in every step and a lot of time spent following up this part of the accounting, I started on this project to simplify the processes. 

Aim for this project was to:

- Automate posting of payments from a partner
- Standardize posting in the accounting system
- Minimize risks for wrong posting
- Minimize risks of sending collections for already paid receivables
- Minimize needs and time associated with employee training
- Facilitate and minimize reconciliation time
- Minimize time for documentation by making transactions easily traceable


Approch:

1. Communication and collaboration with vendor to create files for their payments.  
2. Decide on format of files and design of content inside the files in collaboration with vendor
3. Create a secure exchange platform for the files in collaboration with vendor -> FTP Server
4. Communication and collaboration with internal IT-infrastructure to access the FTP-server, being able to access through a sFTP server and retrievde the files
5. Escalating files for all properties
6. Creating solution to merge XML files into a CSV file with VBA. Must be able to read and imported into the accounting system. Must be easy in use.
7. Creating a CSV-file containg good transaction details making them easily traceable and reconciliated in the accounting system
8. Distribute and communicating the solution to the accounting-department
9. Training, support and bugfixes
10. Handing over responsibility

Process description:

1. User opens up Macro-file, presses button to open up file dialog and select one or multiple xml-files
2. XML-files are imported into a hided sheet with a table that is mapped according to the xml-contents. 
3. Another sheet is configured with functions to retrieve and organize the data into a form that can be imported into Microsoft Dynamics Nav
4. The content of the above sheet is copied and pasted as values into a new sheet
5. The new sheet is exported into a new workbook that is saved and named automatically as a CSV-file.
6. The user imports the CSV-file into Microsoft Dyamics Nav and the transactions are imported into a batch ready to post.
7. While posting the user can get errors and by that getting alerted if there is error in the data from the travel agency or error in the statements of the PMS system. So already at this stage they get alerted and a chance to do necessary correction for easier reconcilation and giving feedback right away to the travel agency or the customer (the hotel).
8. User reconciliates the transactions in the reconciliation system provided by Save Solutions; Account Control.


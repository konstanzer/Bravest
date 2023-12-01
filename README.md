### A Python application for NY Bravest FCU

NY Bravest provides firefighters with loans and benefits and data must be relayed between other financial companies. This app simplifies the communications between a few financial institutions. The application must be stored in the same directory as the associated database file, BravestDB.xlsx.

#### Week 1

The user should have saved an Employee Election spreadsheet with adds and changes for the current week's payroll. Click the top button and a pop-up will ask the user to identify this file. It must be opened throught the app to have the correct format. The user can add records in addition to those already in the spreadsheet. Enter new records at the bottom of the first sheet but do not alter the columns. Save your changes.

The second button down makes a new text file from these records and adds them to the database. The file is named "PNET...txt" and is saved in the current week's directory, ready to be forwarded to the Office of Payroll Administration (OPA.)

#### Week 2

At this point, OPA has recieved a file and replied with the file named "PEDT...txt" indicating the amount of payroll they'll be sending. The third button does a few things. First, it adds a column to store this week's OPA amounts and compares these amounts to the records in the database. Does a member have a different payroll deduction amount in the database? Does the new file include unrecognized members? Were accounts rejected? Payroll totals and discrepancies are listed in a new Excel file with the format "yyyymmdd_analysis.xls," which opens automatically when the process completes.

If no further changes are necessary, create the FC.txt file to forward on to FedComp with the fourth button. If changes are made and a new *winston-all* sheet is needed, oepn the database through the app and new WInston sheet will be created automatically.

### Changelog

**1.2.0** adds the *Generate new Winston sheet* button and *Winston total this week* to the main interface. The *Amount to FedComp* total is deleted on account of redundancy. The *winston-all* sheet is now included in the database file, which is now an Excel workbook and not a csv file. This version adds a *note* column to the *EmployeeElection* sheet. A console window now opens with the application for help with debugging. It also fixes a bug when naming the "PNET...txt" file and another when making newline characters in the FC.txt file.

**1.2.1** Fixed value error raised for mixed integers and datetimes. Now it just skips invalid dates.

**1.2.2** Fixed date column merge error (object and datetime) when adding new records.

**1.2.3** Fixed note column merge error that happened when Employee Election sheet had no notes.

**1.3.0** Small visual improvements. Analysis button now shows totals and discrepant records in Excel rather than the in the GUI and pop-out window. Fixed error that happened when database had stray cells filled.

**1.4.0** Winston_all sheet now sorts by first, last, and MI. EE sheet added "W" option for withhold from OPA but add to Winston sheet.

**1.4.1** Getting 'No engine found for xls' in a new environment. Added the parameter to df.to_excel.

**1.5.0** Several quality of life improvements and a snazzier interface.

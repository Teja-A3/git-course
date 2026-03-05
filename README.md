MAINFRAME COBOL BATCH CASE STUDY 

This Batch case study involves KSDS/PS dataset as input file. 

 

Note: Adhere to the specifications given and naming convention suggested as per standards. 

 

Naming Conventions: <Mainframe ID>.OND25…. 

Example: TRGJ01.OND25.SRCLIB  

Already existing library can be used for the revised case study. 

 

Assignment Number – A001       

Step 1: Creation of Input KSDS/PS Files 

Allocate two input Files of same file attributes - record length – as given in File structure (avg, max) characters - file type – FB and SPACE=(TRK,(5,5)) 

Allocate a new output file with file attributes - record length – as given in File structure (avg, max) characters - file type - FB - SPACE=(TRK,(5,5)) 

 

File 1 name: Employee File-1 

 

Employee Number  

(1-5th byte) type - Numeric 

EID 

(6th byte to 12th byte) 

Alpha-Numeric 

Employee Name 

(13th byte to 32nd byte 

(Alpha-Numeric) 

Location 

(33rd byte to 42nd byte) Alpha only 

Department 

(43rd byte to 52nd byte) Alpha Numeric 

10001 

EIDABCD 

Alex Dev 

Chennai 

HR 

10002 

EIDPQRS 

Bindhu Roy 

Chennai 

Operations 

10006 

EIDLMNO 

Cathy Singh 

Chennai 

Claims 

10009 

EIDSAIL 

Devi kumari 

Chennai 

Billing 

10010 

EIDOSCR 

Earl Gupta 

Hyderabad 

HR 

10005 

EIDONGC 

Freddy Dass 

Hyderabad 

Operations 

10012 

EIDEFGH 

Geetha Pavan 

Hyderabad 

Claims 

10007 

EIDDEEP 

Hari kumar 

Hyderabad 

Billing 

10011 

EIDMSD1 

Irene Jay 

Hyderabad 

HR 

10008 

EIDJACK 

Janani Suresh 

Hyderabad 

Operations 

10004 

EIDXXZZ 

Kunal Rao 

Hyderabad 

Billing 

10013 

EIDA12D 

Lima Reddy 

Hyderabad 

Operations 

10012 

EIDEFGH 

Geetha Pavan 

Hyderabad 

Claims 

10006 

EIDLMNO 

Cathy Singh 

Chennai 

Claims 

10004 

EIDXXZZ 

Obed Rajula 

Hyderabad 

Billing 

10001 

EIDABCD 

Alex Dev 

Chennai 

HR 

 

 File 2 name: Employee File-2 

  

Employee Number (1-5th byte) type - Numeric 

EID 

(6th byte to 12th byte) 

Alpha-Numeric 

Employee Name 

(13th byte to 32nd byte 

(Alpha-Numeric) 

Location 

(33rd byte to 42nd byte) Alpha only 

Department 

(43rd byte to 52nd byte) 

10001 

EIDABCD 

Alex Dev 

Chennai 

HR 

10028 

EIDCCCC 

Balaji Naveen 

Chennai 

PPS 

10006 

EIDLMNO 

Cathy Singh 

Chennai 

Claims 

10009 

EIDSAIL 

Devi kumari 

Chennai 

Billing 

10010 

EIDOSCR 

Earl Gupta 

Hyderabad 

HR 

10005 

EIDONGC 

Freddy Dass 

Hyderabad 

Operations 

10017 

EIDAAAA 

Ahamed Mohi 

Chennai 

CIT 

10020 

EIDZZZZ 

Janani Murugan 

Chennai 

CIT 

10011 

EIDMSD1 

Irene Jay 

Hyderabad 

HR 

10008 

EIDJACK 

Janani Suresh 

Hyderabad 

Operations 

10025 

EIDYYYY 

Raghu Thanga 

Chennai 

RENO 

10004 

EIDXXZZ 

Kunal Rao 

Hyderabad 

Billing 

10030 

EIDBBBB 

Yassar Arafa 

Chennai 

PPS 

  

 

Assignment Number – A002      Assignment Name – COBOL  

First input file should be Employee File 1 created in Assignment A001 

Second input file should be Employee File 2 created in Assignment A001. 

 

Compare the 2 files and write matching records based on Employee Number. If you find a matching record, write the contents of input FILE 1 to output. Write the output into OUTBOTH (FB file of same length as of input file).   

 

This output file should contain   

 

EMPLOYEE NAME  

EMPLOYEE NUMBER  

EMPLOYEE EID  

DEPARTMENT NAME 

SALARY 

BONUS 

 

Don’t write any unmatched record into the output file. Refer point 7 for addition of new field called Salary to the output file. 

 

The output files should not have duplicate entries. Try to eliminate/discard Duplicate records within COBOL program. 

 

For employees belonging to Chennai, Allot 25 thousand dollars and 45 cents as Salary. The Salary field in output file should be the last field and should display in the format 

$ 25,000.45    

Use proper picture clause in the program to achieve this format for Salary field 

For employees belonging to other places, Allot 23 thousand dollars and 65 cents as Salary. 

Once the Base Salary is allotted, introduce a new field named BONUS Percent. Allot 10% Bonus to employees belonging to Hyderabad and 16% to Chennai employees.  

 

Now, introduce a new field named New Salary and calculate the new salary for each employee based on below formula. 

New Salary = base Salary + (Base Salary * Bonus percent /100)  

The output format of New Salary should be same as Base Salary field.  

Example: $ 27,000.95    

 

Prepare a copybook for the output file based on the requirement. This copybook will be used in File manager to view the output file after program execution. So prepare one and keep it ready. 

 

 

DISPLAY the COUNT of records in each input file and output files in below described formats and print it to SYSOUT as follows. 

“EXECUTION OF PROGRAM ENDED” 

“TOTAL NUMBER OF RECORDS IN INPUT FILE-1 IS “    XX    “RECORDS” 

“TOTAL NUMBER OF RECORDS IN INPUT FILE-2 IS “   XX    “RECORDS” 

 “TOTAL NUMBER OF RECORDS IN OUTPUT FILE-BOTH IS “   XX    “RECORDS” 

 

Where XX describes the exact count of records present in that corresponding file. This COUNTS displayed in SYSOUT should MATCH the number of records present in each file.  

Note to Submission: 

Create a document, paste relevant screen shots to include: 

Content in data Files 1 and 2. 

Complete COBOL coding. 

JCL used to RUN the program. 

Output pages from SPOOL and output dataset. Caption each screenshot appropriately and send it within the timeline. 

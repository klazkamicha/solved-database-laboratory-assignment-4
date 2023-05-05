Download Link: https://assignmentchef.com/product/solved-database-laboratory-assignment-4
<br>
Use the company database created in Assignment # 2.

<ul>

 <li>Write a PL/SQL program to raise the salary of employees as follows:</li>

</ul>

All managers: 20% increase

Dno        % of increase

<ul>

 <li>10</li>

 <li>15</li>

 <li>18</li>

</ul>




<ul>

 <li>Write a PL/SQL program to find maximum salary earners name (use cursor)</li>

 <li>Write a PL/SQL program to find top N/2 salary earners name</li>

</ul>

<strong> </strong>




<ol start="2">

 <li>Consider a bank database with only one relation</li>

</ol>

Transaction (transno, acctno, date, amount)

The amount attribute value is positive for deposits and negative for withdrawals

<ul>

 <li>Define an SQL view TP containing the information (accno, T1.date, T2.amount) for every pair of transactions T1, T2 such that T1 and T2 are transactions on the same account and   the date of T2 is  ≤ the date of T1.</li>

</ul>




<ul>

 <li>Using only the above view TP, write a query to find for each account the minimum balance it ever reached (not including the 0 balance when the account is created). Assume there is at most one transaction per day on each account and each account has had at least one transaction since it was created. To simply your query, break it up into 2 steps by defining an intermediate view V.</li>

</ul>




<ol start="3">

 <li>Consider following two relations</li>

</ol>

Book_stock(<strong>Book_id</strong>, Title, No of Copies)

Book_Issue(<strong>card_no</strong>, cholder_name, <strong>book_id</strong>, issue_date, due_date)

Book_Return(<strong>card_no</strong>, cholder_name, <strong>book_id</strong>, return_date, issue_date)




Write a PL/SQL program for issuing/return of books with following conditions:

The program will take option I(issue) / R(return) along with card_no from user. Accordingly, insert records in Issue and Return relations. Date of issue/return must be populated with SYSDATE. Before issuing book, check the following constraints:  A member is not allowed to issue more than 3 books. A member is not allowed to issue more than one copy of same bookid.

After issuing/return of book the no of copies must be updated. If the return date of the book is later than the due date; insert a record in a new table called Fine (card_no, amt). Assume a fixed late fine amt.

<ol start="4">

 <li>Given a relation graph (P,Q, cost) where P and Q attributes represent vertices associated to edges in the graph and cost represent weight.</li>

</ol>

Write SQL/PL-SQL program for the followings

<ul>

 <li>Find the vertices with max and min degree.</li>

 <li>List all the path of length 2 with total cost less than 10.</li>

</ul>

<ol start="5">

 <li>Consider the following Table in a banking database:</li>

</ol>

Account(<strong>Accno</strong>, Accname, Type, Balance)

Write a PL/SQL program for withdraw and deposit of amount on a given account with following features:  The program should check conditions for insufficient fund (before withdraw) and raise error. For successful transaction, the program must update Account relation and subsequently insert records of the transactions in a new table called Transaction with following definition:

<strong>                            Transaction</strong>(Tr_id, Accno, Tr_type, Amt, date of Tr)







<strong> </strong>

<strong> </strong>

<strong>Database Laboratory Assignment # 4 </strong>

<ol>

 <li>Write database triggers for Q 3 and Q 5 of Assignment # 3. Test the correctness of the triggers with relevant DML operations (e.g. issue/return of books, withdraw/deposit transactions on account)</li>

</ol>




<ol start="2">

 <li>Consider the following relations for an OPD in an hospital:</li>

</ol>

Patient(patient-id, patient-name, DOB, Sex)

Doctor(Doctor-id, Name, specialization, Unit)

OPD_Schedule(Doctor-id, date, time, fees)

Appointment (appointment-no, patient-id, doctor-id, date) OPD_payments(appointment-no, patient-id, amt, date_payment) Write SQL/PL-SQL program for the following tasks:

<ul>

 <li>Display the list of patients who has visited the same doctor in the hospital more than 2 times during a given time-period</li>

 <li>The records in OPD_payments to be automatically updated based on Schedule and Appointment table. If a patient visits twice the same doctor within a week, amt in OPD_payments will be automatically set to 0. For senior citizen female patients, the fees to be reduced by 50% and entry should be automatically inserted in OPD_payments table.</li>

 <li>Display the number of patients visited to the doctors unit-wise and date-wise.</li>

 <li>Change the date and time (not other field) in OPD_Schedule of any given doctor through views.</li>

 <li>Create a OPD log including patient name, age, date_of_visits and doctor names for a given period.</li>

 <li>Increase the fees of a given doctor through views.</li>

</ul>







<ol start="3">

 <li>Consider the following database:</li>

</ol>

Student(Sroll, Name, Branch, Batch, Programme)

Course(CID, Cname, Instructor Name)

Attendance(Sroll, Course ID, Period, Total#class, Attendance)

Period includes start-date and end-date, Total#class states total number of classes conducted during a period.

Write SQL/PL-SQL program for the following tasks:

<ul>

 <li>Display the name of students whose attendance is below 80% in a given course.</li>

 <li>Create a view to list attendance records of the students in all subjects for a given batch.</li>

 <li>Use the view in (ii) to list the student names whose attendance is below 70% in all the subjects.</li>

 <li>Create a view to display attendance of students for a given course ID.</li>

 <li>Use this view in (iv) to update the attendance of a student (assume the update is done by a authorized user)</li>

 <li>Internal marks for attendance for a student is to be calculated against a course as per the following rules:</li>

</ul>




Attendance % Marks

&gt;=95                5

85-95                4

75-85                3

60-75                2

&lt; 60                  0




Write a PL/SQL function which takes sroll and course id as input and computes the attendance percentage for that course and returns the marks for that course. Then, Insert the Sroll and Marks in a newly created table called ATT_Marks(Sroll, course-id, Marks). This complete task is to be done in a single PL/SQL program.



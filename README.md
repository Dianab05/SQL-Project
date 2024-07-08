<h1>Database Project for Booking</h1>

The scope of this project is to use all the SQL knowledge gained throught the Software Testing course and apply them in practice.

Application under test: **Booking**

Tools used: **MySQL Workbench**

**Database description:** <br>

In this project, I created a SQL database inspired from the Booking application. <br> 
The purpose of the database is to store and manage the necessary information for travel reservations, including details about users, properties, bookings, and reviews. <br> 
The database will ensure data integrity and accessibility, facilitating the operations of storing, querying, updating, and deleting relevant data for the efficient functioning of the application. <br>

**General Information Stored** <br>

**Bookings** <br>
Information about bookings, such as user ID, property ID, check-in and check-out dates, and booking status (pending, confirmed, canceled). <br>

**Users** <br>
Personal information of users, such as first name, last name, birth date, email, and role (client or owner).

**Properties** <br>
Details about properties, including property name, description, address, city, country, price per night, capacity, and availability. <br>

**Payments** <br> 
Payment details, including booking ID, payment method (credit card, cash), amount paid, and payment date. <br>

**Reviews** <br>
User evaluations and comments about properties, including rating, description, and review date. <br>

<ol>
<h4> <li> Database Schema </li> </h4>

You can find below the database schema that was generated through Reverse Engineer and which contains all the tables and the relationships between them.

![Booking reverse engineer](https://github.com/Dianab05/SQL-Project/assets/166596469/488e1321-ad66-430e-b44c-06879b8ec41a)


The tables are connected in the following way:
<ul>
  
**<li>Users** is connected with **Bookings** through a **one-to-many** relationship which was implemented through Users.user_id as a **primary key** and Bookings.user_id as a **foreign key**.</li>
**<li>Properties** is connected with **Bookings** through a **one-to-many** relationship which was implemented through Properties.property_id as a **primary key** and Bookings.property_id as a **foreign key**.</li>
**<li>Bookings** is connected with **Payments** through a **one-to-one** relationship which was implemented through Bookings.booking_id as a **primary key** and Payments.booking_id as a **foreign key**.</li>
**<li>Properties** is connected with **Reviews** through a **one-to-many** relationship which was implemented through Properties.property_id as a **primary key** and Reviews.property_id as a **foreign key**.</li>
**<li> Users** is connected with **Reviews** through a **one-to-many** relationship which was implemented through Users.user_id as a **primary key** and Reviews.user_id as a **foreign key**.</li>
</ul>

<h4><li>Database Queries</li></h4>

<ol type="I">
  
<h4><li>DDL (Data Definition Language)</li></h4>

The following instructions were written in the scope of CREATING the structure of the database (CREATE INSTRUCTIONS). <br>

![create11](https://github.com/Dianab05/SQL-Project/assets/166596469/998b1ce1-b2cc-4ff6-ac0c-8204e53e57aa)

![create1](https://github.com/Dianab05/SQL-Project/assets/166596469/f6d8e44f-9fb6-4520-a509-fb177e4174e1)

 ![create2](https://github.com/Dianab05/SQL-Project/assets/166596469/c6ebb053-bbf8-4dc5-8071-34515bc1f08e)

 ![create 3](https://github.com/Dianab05/SQL-Project/assets/166596469/c8e9853d-957f-4de5-ab71-ba8187936870)

![create4](https://github.com/Dianab05/SQL-Project/assets/166596469/c9f582da-1cbc-4830-a57f-00b6415f586e)

![create5](https://github.com/Dianab05/SQL-Project/assets/166596469/3d57ae8c-fd8a-4e4d-add2-3cb00117b901)



  After the database and the tables have been created, a few ALTER instructions were written in order to update the structure of the database, as described below: 
  <ul>
<li>Changing the Table Name </li>

![alter11](https://github.com/Dianab05/SQL-Project/assets/166596469/a6297c80-3dda-41d5-9152-b3b024f6e36a)

<li>Adding or Dropping Columns </li>

![alter3](https://github.com/Dianab05/SQL-Project/assets/166596469/be4ba0f5-573b-442d-9dea-eac2a423e688)

<li>Renaming Columns </li>

![alter12](https://github.com/Dianab05/SQL-Project/assets/166596469/9abe73a4-f4ca-4540-96bb-d584502d1deb)

<li>Adding Column Properties </li>

![alter4](https://github.com/Dianab05/SQL-Project/assets/166596469/df7b793c-0591-4e43-b6a3-ee6a83cfe80c)

<li>Modifying Column Properties </li>

![alter5](https://github.com/Dianab05/SQL-Project/assets/166596469/8ec10c1c-2e29-46f4-8095-c1226d8fc48e)

<li>Adding Primary or Foreign Keys </li>

![alter6](https://github.com/Dianab05/SQL-Project/assets/166596469/75abe2e5-b9e3-47e0-928f-ef2e5bdf9768)


![alter2](https://github.com/Dianab05/SQL-Project/assets/166596469/2365df44-1e33-4fbb-b36f-094aa3bf2951)

</ul>


<h4> <li>DML (Data Manipulation Language)</li> </h4>

  In order to be able to use the database I populated the tables with various data necessary in order to perform queries and manipulate the data. 
  In the testing process, this necessary data is identified in the Test Design phase and created in the Test Implementation phase. 

  Below you can find some of the **INSERT** instructions that were created in the scope of this project:

![insert1](https://github.com/Dianab05/SQL-Project/assets/166596469/e1fcc2e2-b82a-403e-baff-d9520e53bbc7)

![insert 2](https://github.com/Dianab05/SQL-Project/assets/166596469/6e545269-16d3-4942-813d-322d57e11769)

![insert22](https://github.com/Dianab05/SQL-Project/assets/166596469/bd649fee-27c8-4da8-a15e-a697e3e50c60)

![insert3](https://github.com/Dianab05/SQL-Project/assets/166596469/7a8345ec-9fb0-4d1f-ad6a-069c599f101d)

![insert4](https://github.com/Dianab05/SQL-Project/assets/166596469/9a12006f-4375-4915-b258-87adca7ade04)


  After the insert, in order to prepare the data to be better suited for the testing process, I updated some data in the following way. 
  Below you can find some of the **UPDATE** instructions that were created
  
![update1](https://github.com/Dianab05/SQL-Project/assets/166596469/1b2bb152-0de9-49f5-8c53-20305626163c)

![update2](https://github.com/Dianab05/SQL-Project/assets/166596469/12250f25-261f-46c3-8b41-665727a78fb2)

![update3](https://github.com/Dianab05/SQL-Project/assets/166596469/bdb15184-4733-454a-9141-9fc08fafd49a)

![update4](https://github.com/Dianab05/SQL-Project/assets/166596469/e46d6b13-1666-4c7a-aa2b-7e8cfb5d034f)

![update5](https://github.com/Dianab05/SQL-Project/assets/166596469/27345264-ff64-49a3-b2ef-603fbaf86380)



  
  **Inserati aici toate instructiunile de UPDATE pe care le-ati scris folosind filtrarile necesare astfel incat sa actualizati doar datele de care aveti nevoie**


 <h4> <li>DQL (Data Query Language)</li> </h4>
 
After the testing process, I deleted the data that was no longer relevant in order to preserve the database clean: 

**Inserati aici toate instructiunile de DELETE pe care le-ati scris folosind filtrarile necesare astfel incat sa stergeti doar datele de care aveti nevoie**

In order to simulate various scenarios that might happen in real life I created the following queries that would cover multiple potential real-life situations:

**Inserati aici toate instructiunile de SELECT pe care le-ati scris folosind filtrarile necesare astfel incat sa extrageti doar datele de care aveti nevoie**
**Incercati sa acoperiti urmatoarele:**<br>
**- where**<br>
**- AND**<br>
**- OR**<br>
**- NOT**<br>
**- like**<br>
**- inner join**<br>
**- left join**<br>
**- OPTIONAL: right join**<br>
**- OPTIONAL: cross join**<br>
**- functii agregate**<br>
**- group by**<br>
**- having**<br>
**- OPTIONAL DAR RECOMANDAT: Subqueries - nu au fost in scopul cursului. Puteti sa consultati tutorialul [asta](https://www.techonthenet.com/mysql/subqueries.php) si daca nu intelegeti ceva contactati fie trainerul, fie coordonatorul de grupa**<br>

</ol>

<li>Conclusions</li>

**Inserati aici o concluzie cu privire la ceea ce ati lucrat, gen lucrurile pe care le-ati invatat, lessons learned, un rezumat asupra a ceea ce ati facut si orice alta informatie care vi se pare relevanta pentru o concluzie finala asupra a ceea ce ati lucrat**

</ol>

# Class Database

## Submission

Below you will find a set of tasks for you to complete to consolidate and extend your learning from this week.  You will find it beneficial to complete the reading tasks before attempting some of these.

To submit this homework write the correct commands for each question here:

```sql
1.select * from rooms where rate >100;
2. select * from reservations where checkin_date between '01-09-2020' a
nd '30-09-2020' and checkout_date-checkin_date > 3;
3.select * from customers where name like 'M%';
4. insert into room_types (room_type,def_rate) values ('PENTHOUSE',185.
0);
5. insert into rooms (room_no,room_type,rate) values(501,'PENTHOUSE',18
5),(502,'PENTHOUSE',185);
6. insert into rooms (room_no,room_type,rate) values(503,'PREMIUM PLUS'
,143);
7. select count(room_no) from reservations where checkin_date between '
01-08-2020' and '30-08-2020' and checkout_date-checkin_date >0;
8. select sum(checkout_date - ckeckin_date) from reservations where roo
m_no between 201 and 299;
9. select count(total),sum(total),round(avg(total)) from invoices where
 total > 300;
10. select sum(checkout_date - checkin_date) as Number_of_nights,floor(r
oom_no/100) as floor_number from reservations group by floor(room_no/100) having
 floor(room_no/100)>0 order by floor_number;

```

When you have finished all of the questions - open a pull request with your answers to the `Databases-Homework` repository.

## Homework

If you haven't completed all the exercises from this lesson then do that first.

### Tasks
1.  Which rooms have a rate of more than 100.00?
2.  List the reservations that have a checkin date this month and are for more than three nights.
3.  List all customers from cities that begin with the letter 'M'.

Insert some new data into the room_types and rooms tables, querying after each stage to check the data, as follows:

4.  Make a new room type of PENTHOUSE with a default rate of £185.00
5.  Add new rooms, 501 and 502 as room type PENTHOUSE and set the room rate of each to the default value (as in the new room type).
6.  Add a new room 503 as a PREMIER PLUS type similar to the other PREMIER PLUS rooms in the hotel but with a room rate of 143.00 to reflect its improved views over the city.

Using what you can learn about aggregate functions in the w3schools SQL classes (or other providers), try:

7.  The hotel manager wishes to know how many rooms were occupied any time during the previous month - find that information.
8.  Get the total number of nights that customers stayed in rooms on the second floor (rooms 201 - 299).
9.  How many invoices are for more than £300.00 and what is their grand total and average amount?
10.  Bonus Question: list the number of nights stay for each floor of the hotel (floor no is the hundreds part of room number, e.g. room **3**12 is on floor **3**)

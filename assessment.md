```sql

-- create a customer table 
create table customer (customer_id int, cust_name varchar(20),city varchar(20),grade int , salesman_id int);

-- insert the value in customer table 
insert into customer value
(3002,"nike rimando","new york",100,5001),
(3007,"brad davis","new york",200,5001),
(3005,"graham zusi","california",200,5002),
(3008,"julian green","london",300,5002),
(3004,"fabion johnson","peris",300,5006),
(3009,"geoff cameron","berlin",200,5003),
(3003,"jozy altidor","moscow",100,5007),
(3001,"brad guzan","london",null,5005);



--create a salesman table 
create table salesman( salesman_id int, name varchar(20), city varchar(20) ,commission decimal(10,2));

-- insert the value in salesman table 
insert  into salesman value
(5001,"jamesh hoog","new york",0.15),
(5002,"nail knite","paris",0.13),
(5005,"pit alex","london",0.11),
(5006,"mc lyon","paris",0.14),
(5007,"paul adam","rome",0.13),
(5003,"lauson hen","sun jose",0.12);

/* SQL query to find the salesperson(s) and the 
customer(s) represented here. Return the Customer Name, City, Salesman, 
commission. */
SELECT 
  customer.cust_name ,
  customer.city ,
  salesman.name ,
  salesman.commission 
FROM customer
inner JOIN salesman 
ON customer.salesman_id = salesman.salesman_id;

```
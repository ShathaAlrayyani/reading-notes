## Introduction to SQL
## Like:

***Like is similar to equal*** 

**For example:**

If I want to find names start with A :

Where name Like "A%"

If I want to find names end with s :

Where name Like "%s"

If I want to find names start with b and end with r :

Where name Like "b%r"

if I want to find a word and don't know its exact position in a string :

Where e-mail Like "%gmail%"

the output will be every email contains "gmail"

## In:
**In is similar to = but for more than one value.**

**For example :**

If I'm working for a company and I want to see all the information about Walmart and Apple :

Where name In ('Walmart' , 'Apple')

If I want to do the same by using the IDs

Where Id In (1001 , 1002)

**you can use as many values as you want just make sure to separate them using comma.**


## Between & And :
**we use them if we have more than one condition with Where ,also you can use them with calculations  ( *,+,-,/) or even with ( Not , Like ,In )**

**For example :**
if I want to see the data for IDs between 1001 & 1010  :

Where  Id >= 1001 AND id <= 1010

or we can write it in a different way:

Where Id Between 1001 AND 1010

If I want to see names start with A and there Id more than 1050 :

Where  names Like 'A%'  AND  id >1050
this command will send me names start with A who have id > 1050  only.


## Or :
we use it when we have MORE than one condition and we want at least one of them to be true.

**For example :**

if I want to see names start with B or H :

***Where*** names ***Like*** 'B%' ***OR*** names ***Like*** 'H%'

this will show me names they start with B and names start with H 
but if there is no names start with H it will show me names start with B only , vice versa.



**To understand how to use join there are a couple of things need to know first :**

1 - Primary Key : is a special key which uniquely identifies each record in a table , must be in the first column , and it might have a different name in each one

2- Foreign key : it establishes a link between records in two different tables in a database. It can be a column in a table that points to the primary key columns meaning a foreign key defined in a table refers to the primary key of some other table. and it might have a different name

**in simple way : every Foreign Key is a Primary Key in another table**



## Join :
is used to combine rows from two or more tables, based on a related column between them.

we have 4 types of JOIN
inner join = join
left join
right join
outer join = full outer join

how to use join :

Select column1,column2 ,... etc . Or you can Select * for all the columns

From table 1  ---> left table

Join table 2   ----> right table

On table1.pk_name = table2.fk_name

**For more information please see my Note** [here](https://miro.com/app/board/uXjVOvB7w3E=/)


![](task%20sql1.png)
![](task%20sql2.png)
![](task%20sql3.png)
![](task%20sql4.png)
![](task%20sql5.png)
![](task%20sql6.png)
![](task%20sql13.png)
![](task%20sql14.png)
![](task%20sql15.png)
![](task%20sql16.png)
![](task%20sql17.png)
![](task%20sql18.png)
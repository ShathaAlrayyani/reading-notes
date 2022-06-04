## Introduction to SQL
## Like:
**Like is similar to equal **
**For example:**
</br> </br>
If I want to find names start with A :</br>
Where name Like "A%"</br>
</br>
If I want to find names end with s :</br>
Where name Like "%s"</br>
</br>
If I want to find names start with b and end with r :</br>
Where name Like "b%r"</br>
</br>
if I want to find a word and don't know its exact position in a string :</br>
Where e-mail Like "%gmail%"</br>
</br>
the output will be every email contains "gmail"

## In:
**In is similar to = but for more than one value.**
</br>
**For example :**
</br> </br>
If I'm working for a company and I want to see all the information about Walmart and Apple :</br>
Where name In ('Walmart' , 'Apple')</br>
</br>
If I want to do the same by using the IDs</br>
Where Id In (1001 , 1002)</br>
</br>
**you can use as many values as you want just make sure to separate them using comma.**
</br>
## Between & And :
**we use them if we have more than one condition with Where ,also you can use them with calculations  ( *,+,-,/) or even with ( Not , Like ,In )**
</br>
**For example :** </br> </br>
if I want to see the data for IDs between 1001 & 1010  :</br>
Where  Id >= 1001 AND id <= 1010</br>
</br>
or we can write it in a different way:</br>
Where Id Between 1001 AND 1010</br>
</br>
If I want to see names start with A and there Id more than 1050 :</br>
Where  names Like 'A%'  AND  id >1050</br>
this command will send me names start with A who have id > 1050  only.</br>
</br>

## Or :
we use it when we have MORE than one condition and we want at least one of them to be true.
</br>
**For example :** </br>
</br>
if I want to see names start with B or H :</br>
***Where*** names ***Like*** 'B%' ***OR*** names ***Like*** 'H%'</br>
</br>
this will show me names they start with B and names start with H </br>
but if there is no names start with H it will show me names start with B only , vice versa</br>



